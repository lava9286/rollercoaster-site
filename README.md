# rollercoaster-site
rollercoaster_info = {
    "title": "My Custom Rollercoaster",
    "intro": "A rollercoaster I designed and built with epic drops, twists, and turns!",
    "design": """I built this rollercoaster using wood, screws, and a lot of testing.
                 It took weeks of planning, modeling, and hard work to bring it to life.""",
    "features": {
        "First Drop": "12 feet at 60°",
        "Twists": "3 loops and sharp turns",
        "Top Speed": "30 mph",
        "Track Length": "50 feet"
    },
    "experience": "It’s thrilling from start to finish! Friends say it’s better than some real theme parks."
}

html_content = f"""
<!DOCTYPE html>
<html>
<head>
    <title>{rollercoaster_info['title']}</title>
</head>
<body>
    <h1>🎢 {rollercoaster_info['title']}</h1>
    <p>{rollercoaster_info['intro']}</p>

    <h2>🛠️ Design & Engineering</h2>
    <p>{rollercoaster_info['design']}</p>

    <h2>🎯 Features</h2>
    <ul>
        {''.join(f"<li>{k}: {v}</li>" for k, v in rollercoaster_info['features'].items())}
    </ul>

    <h2>🎉 Ride Experience</h2>
    <p>{rollercoaster_info['experience']}</p>

    <footer>
        <p>Built by You • All thrills reserved 🎠</p>
    </footer>
</body>
</html>
"""

# Write to a file
with open("rollercoaster_website.html", "w") as f:
    f.write(html_content)

print("✅ Website generated! Open 'rollercoaster_website.html' in your browser.")
