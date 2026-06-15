My First Ever Exoplanet Transit Detector

Hi everyone! This is my very first real programming project, which I built as a high school student. 

The inspiration for this project came from citizen science projects on Zooniverse. I spent a lot of time looking at those deep-green stellar light-curve scatter plots, 
trying to spot planet transit signals by eye. Then I thought: *Can I write an algorithm to make the computer do this automatically? Can it find that exact dip where a planet 
blocks a star's light, and calculate its orbital period all on its own?

This web app was now born!

---

 Try the Live Demo!
I deployed this project onto a cloud server so that anyone in the world can play with it directly in their browser:
https://transit-detector-8uaveshqbbzvwz8cebjmapp.streamlit.app/

---

What Can This App Do?

1. Analyze Uploaded Images: You can take a screenshot of a stellar scatter plot from Zooniverse and upload it. I wrote an image-processing algorithm that reads the pixel trends from the photo, recreates a high-contrast scientific plot on the right, and highlights the potential planet transit regions with bright fuchsia spans!
2. Live NASA Data Integration: If you don't have an image, you can type a real star identifier (like TOI-270 or Pi Mensae) on the left. My Python backend will connect directly to NASA's official MAST archive in real-time, download the raw satellite data, and plot it instantly!
3. Dynamic Period Calculation: The algorithm measures the distance between those fuchsia transit blocks and uses physics math to deduce exactly how many days the planet takes to complete one orbit in space.
4. Similar Planet Matchmaker: Once the orbital period is calculated, the app searches an built-in database to find real, confirmed exoplanets discovered by astronomers (like the famous TRAPPIST-1 family) that share a similar orbital period, adding a cool educational touch.
5. 7-Language Support: There is a dropdown menu in the top right corner that allows you to switch the entire interface between English, Simplified Chinese, Japanese, Russian, French, German, and Spanish.

---

 My Tech Toolbox

To build this, I had to learn a bunch of advanced Python libraries that I had never heard of before:
- Streamlit: Used to quickly build and layout this dark, space-themed interactive dashboard.
- Numpy & Pillow: Used to convert image pixels into numerical arrays for the algorithm to analyze.
- Matplotlib: Used to generate high-quality, scientific-style scatter plots with a deep-space grid.
- Lightkurve & Astropy: Specialized astrophysics libraries used to safely request and download official data from NASA's archives.


