📍 Category System for Map UI

A clean, scalable category system used — Map UI, providing consistent icons and readable labels for all map categories.
This module is used to:

Render category sections in the sidebar

Display icons on the map

Generate readable category names in popups

Automatically handle unknown / uncategorized items

✨ Features

🎨 Beautiful emoji-based category icons

🏷️ Human-readable labels for UI sections

🧠 Automatic fallback for unknown categories

🔄 Fully dynamic — add new categories instantly

📱 Perfect for web UI, mobile bottom sheets, and popups

📦 Category Icons

Each category has a unique emoji icon to make navigation more intuitive.

const CATEGORY_ICONS = {
  attraction: "⭐",
  museum: "🏛️",
  restaurant: "🍽️",
  hotel: "🏨",
  beach: "🏖️",
  park: "🌳",
  mall: "🛍️",
  shopping: "🛒",
  cafe: "☕",
  mosque: "🕌",
  church: "⛪",
  gas: "⛽",
  airport: "✈️",
  bus: "🚌",
  train: "🚆",
  school: "🏫",
  university: "🎓",
  hospital: "🏥",
  pharmacy: "💊",
  bank: "🏦",
  office: "🏢",
  stadium: "🏟️",
  playground: "🛝",
  supermarket: "🛒",
  parking: "🅿️",
  police: "🚓"
};

🏷️ Category Labels

User-friendly names for sections, lists, and tooltips.

const CATEGORY_LABELS = {
  attraction: "Attractions",
  museum: "Museums",
  restaurant: "Restaurants",
  hotel: "Hotels",
  beach: "Beaches",
  park: "Parks",
  mall: "Malls",
  shopping: "Shopping",
  cafe: "Cafés",
  mosque: "Mosques",
  church: "Churches",
  gas: "Fuel Stations",
  airport: "Airports",
  bus: "Bus Stations",
  train: "Train Stations",
  school: "Schools",
  university: "Universities",
  hospital: "Hospitals",
  pharmacy: "Pharmacies",
  bank: "Banks",
  office: "Offices",
  stadium: "Stadiums",
  playground: "Playgrounds",
  supermarket: "Supermarkets",
  parking: "Parking Areas",
  police: "Police Stations"
};

🧠 How It Works

When the map loads data:

It checks category in CATEGORY_ICONS

If found → uses its emoji

It checks category in CATEGORY_LABELS

If found → displays its human-readable label

If not found:

Icon defaults to 📍

Label becomes “Other Places”

This keeps the UI clean, organized, and future-proof.

➕ Adding a New Category

To add a new type:

Choose an emoji icon

Add a readable label

Example:

CATEGORY_ICONS.waterpark = "💦";
CATEGORY_LABELS.waterpark = "Water Parks";


Then your JSON can include:

{
  "id": "yas-waterworld",
  "name": "Yas Waterworld",
  "category": "waterpark",
  "lat": 24.49,
  "lng": 54.6
}


Automatically appears in sidebar + markers. ✨

📁 Example JSON (map-data.json)
{
  "places": [
    {
      "id": "sweihan-palms-farm",
      "name": "Sweihan Palms Farm",
      "category": "attraction",
      "label": "Farm • Holiday Home",
      "location": "Sweihan, Al Ain",
      "lat": 24.442,
      "lng": 55.332
    }
  ]
}

🧪 Fallback Behavior

If your data contains:

"category": "xyz"


And no icon/label exists:

Shows 📍 Other Places

Prevents UI breaking

Keeps sidebar clean

📂 Where This Is Used

map.html

Sidebar dynamic category renderer

Marker popup builder

Mobile bottom-sheet UI

📜 License

This category system is part of the Blue Sky Property map interface.
You may reuse, modify, and extend it within your projects.
