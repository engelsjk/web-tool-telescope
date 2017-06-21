# web-tool-telescope

<img src="screenshots/telescope-logo.png" height="300px" width="auto">

<h1>Introduction</h1>
<p>
Telescope was a web-tool used to access and analyze data related to the development of a wind farm, specifically aspects of power performance testing of wind turbines related to the international standard IEC 61400-12-1. It allowed the user to review the geographical layout of a wind farm and provided interactive features for selecting optimal locations of test turbines and meteorelogical towers using complex geospatial analysis.
</p>
<p>
Telescope was an internal web-tool I developed in the wind industry a couple of years ago and is probably still the most complex technical web development project I've worked on to date. It was the culmination of my earliest experimentation with web development, and the most complex in a series of web tools I developed to support techanical support and sales at an international wind turbine manufacturing company. 
</p>

<h1>Motiviation</h1>
<p>
The primary motivation for building this tool was to provide (1) increased knowledge sharing of technical data across multiple groups around the world and (2) an efficienct process for a technical analysis that had previously been done manually. This tool relied upon another internally developed, proprietary desktop client program that was used by analytics teams globally to track and analyze wind farm layout information. Any information that was entered and/or processed by the desktop client program was stored in a centralized database allowing for other users around the globe (with the same client program) to access the information and work seamlessly across projects. 
</p>
<p>
I'm still incredibly proud of this project and it represents some of my most valued professional strengths: identifying issues with efficiency and knowledge sharing, reverse-engineering systems and figuring out how to use new tools, ...
</p>
<p>
This write-up covers the five main components of Telescope: Project, Turbines, Met, PPT and Terrain. In the following sections, I'll provide a brief write-up of each component, both in terms of functionality and development. No source code is included.
</p>

<h1>Main Page</h1>
<img src="screenshots/telescope-1.png" height="500px" width="auto">
<p>
Telescope was a single-page application with a primary map and a secondary information display area. The front-end was built primarily using HTML/CSS, Javascript, jQuery, underscore, D3 and Leaflet. The back-end was built on a relatively simple structure of Python scripts called via CGI, all running on a Windows IIS web server. Telescope (and other web tools) was hosted on a virtual machine set up by the company's internal IT department but largely configured, operated and monitored by myself.
</p>
On web tool loading, a sequence of Python scripts were called to query data from a central application server operated by a team of internal developers in Europe. This initial loading query was used to populate a set of select boxes with lists of wind farm projects and the countries and regions they reside in. After this is done, the loading screen (top image) disappears and the main page (map, select boxes, blank information box, etc) appears.
<p>
<p>
The user can then select regions or countries, and the map will zoom in to the respective area and show markers on the map for each wind farm project location. Once the user selects a specific project, the project information appears.
<p/>

<h1>Project</h1>
<img src="screenshots/telescope-2.png" height="500px" width="auto">
<p>
The Project information page highlights information about the layout of a project. Each project is version controlled by the client software that is used to create the project, updated by the various project developers who work on the project. Each version also includes a number of different layouts that the project developer has created in the client software, to try out different combinations of turbine types, locations, wind farm control features, etc. The user can select through the different project versions and layouts, and the information associated with these specific layouts is then presented on the page.
</p>
<p>
This information includes the following:
<ul>
<li>Map markers for each turbine location, both new turbines (green) and older turbines (red).</li>
<li>Project coordinates.</li>
<li>Select boxes of project versions and layouts.</li>
<li>A button to export the selected project version/layout to a Google Earth KML file, downloaded in the browser.</li>
<li>Details specific to the layout, such as number of turbines, measured wind conditions, expected production output, etc.</li>
<li>Contact information for the project developer, including a photo and hotlinks for emails with pre-populated subject lines and for instant messenging.</li>
</ul>
</p>
<p>
When a specific project version and layout has been selected, the user can then select through the navigation tabs to use different components of Telescope, including the Turbine tab.
</p>

<h1>Turbines</h1>
<img src="screenshots/telescope-3.png" height="500px" width="auto">
<p>
</p>

<h1>Met</h1>
<img src="screenshots/telescope-4.png" height="500px" width="auto">

<h1>PPT</h1>
<img src="screenshots/telescope-5.png" height="500px" width="auto">

<h1>Terrain</h1>
<img src="screenshots/telescope-6.png" height="500px" width="auto">


