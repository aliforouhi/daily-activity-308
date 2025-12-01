# daily_update.py
import datetime
import random

print("Daily GitHub activity - Day 30")

today = datetime.date.today()

# Generate random RGB colors and calculate brightness
colors = [(random.randint(0,255), random.randint(0,255), random.randint(0,255)) for _ in range(5)]

def brightness(rgb):
    r, g, b = rgb
    return round(0.299*r + 0.587*g + 0.114*b, 2)

brightness_values = [brightness(c) for c in colors]

print(f"Today's date: {today}")
print("Generated RGB colors:", colors)
print("Brightness values:", brightness_values)
print("Brightest color:", colors[brightness_values.index(max(brightness_values))])
