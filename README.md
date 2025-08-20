# Vehicle Valuator Mock (Local Demo)

This is a **fully local mock demo** of a vehicle valuation tool.  
It was adapted from the original version to remove all API calls, instead generating **mock vehicle data** and valuations directly in the browser.

## Features

- 🔑 Enter any **fake registration number** to generate a deterministic mock vehicle record.
  - Make, model, year, variant, and body style are generated locally (same reg = same vehicle).
- 🛠️ If the lookup is wrong, you can edit the vehicle details manually.
- 📏 Enter a **mileage** value to get a mock valuation for that vehicle.
  - The valuation is based on year, model, and mileage bands, with a small random-like jitter to make values more natural.
- 🎉 Fun confetti effect when showing a valuation.

## How it works

- The registration number is hashed and used to pick values from mock datasets (Yamaha, Honda, Suzuki, etc.).
- Mileage depreciation reduces the valuation in set bands (10k+, 20k+, 40k+, etc.).
- A small deterministic jitter ensures valuations don’t look too round/repetitive.

## Usage

1. Open `vehicle_valuator_mock_local.html` in any modern browser (no server required).
2. Enter a fake reg (e.g., `ABC123`).
3. Vehicle details will be displayed. Adjust manually if needed.
4. Enter mileage (e.g., `25000`) and get a mock valuation.

## Notes

- 100% offline – no external API calls.
- Built for demo/testing purposes only (not real valuations).
- Confetti library is loaded from CDN, favicon uses Twemoji (bike emoji).
