<h1>Route-Finding Web App</h1>
<p>A Flask-based route-finding application that calculates and visualizes the optimal path between a source and destination based on user-selected transport mode (walking, biking, driving, or bus). It provides travel time estimates and route visualization using OpenStreetMap data.</p>

<h2>Features</h2>
<ul>
    <li><span class="highlight">Multi-Mode Routing:</span> Choose between walking, biking, driving, and bus modes.</li>
    <li><span class="highlight">Interactive Map Visualization:</span> Visualize the route on an interactive map.</li>
    <li><span class="highlight">Travel Distance and Time Calculation:</span> Get real-time travel distance and estimated time based on mode.</li>
</ul>

<h2>Project Structure</h2>
<pre><code>.
├── app.py                # Main Flask app
├── templates
│   └── index.html        # Main HTML template for frontend
├── static
│   └── style.css         # Optional custom styles
└── README.md             # Project README file
</code></pre>

<h2>Setup and Installation</h2>
<p>Follow these steps to set up and run the project:</p>
<ol>
    <li>Clone this repository:</li>
    <pre><code>git clone https://github.com/yourusername/route-finding-web-app.git</code></pre>
    <li>Navigate to the project directory:</li>
    <pre><code>cd route-finding-web-app</code></pre>
    <li>Install the required dependencies:</li>
    <pre><code>pip install -r requirements.txt</code></pre>
    <li>Run the Flask application:</li>
    <pre><code>python app.py</code></pre>
    <li>Open a web browser and go to <a href="http://127.0.0.1:5000">http://127.0.0.1:5000</a> to access the app.</li>
</ol>

<h2>Usage</h2>
<ol>
    <li>Enter the <strong>source</strong> and <strong>destination</strong> locations.</li>
    <li>Select the mode of transportation: walking, biking, driving, or bus.</li>
    <li>Submit to view the optimal route, travel distance, and estimated time.</li>
</ol>

<h2>Technologies Used</h2>
<ul>
    <li><strong>Flask:</strong> Backend framework for handling HTTP requests.</li>
    <li><strong>Geopy:</strong> For geolocation lookup of addresses.</li>
    <li><strong>OSMNX:</strong> For accessing OpenStreetMap data and building graphs.</li>
    <li><strong>NetworkX:</strong> For calculating shortest paths in transportation networks.</li>
    <li><strong>Folium:</strong> For generating interactive map visualizations.</li>
</ul>

<h2>Example Code</h2>
<pre><code>from flask import Flask, request, jsonify
from geopy.geocoders import Nominatim
import osmnx as ox
import networkx as nx
import folium

app = Flask(__name__)
geolocator = Nominatim(user_agent="route_finder_app")

@app.route('/get-route', methods=['POST'])
def get_route():
    # Fetch source, destination, and mode from request
    # Compute route, time, and distance
    # Generate map with Folium
    pass
</code></pre>

<h2>Screenshots</h2>
<p>Here's a quick look at the app in action:</p>
<img src="screenshot.png" alt="App Screenshot">

<h2>License</h2>
<p>This project is licensed under the MIT License - see the <code>LICENSE</code> file for details.</p>

</body>
</html>
