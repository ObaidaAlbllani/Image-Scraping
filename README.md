# Google Image Scraper & Dataset Builder

An advanced, automated Python service designed to scrape raw high-quality image data directly from Google Search. This project represents a major architectural upgrade from the previous Pinterest scraper, moving towards a robust, engine-agnostic algorithm.

## 🎯 Project Purpose & Core Goal
The primary objective of this project is **educational**—specifically focusing on studying automated data collection workflows and understanding how to programmatically build custom datasets for machine learning and computer vision applications. 

> [!WARNING]
> **Legal & Educational Disclaimer:** This repository is strictly intended for educational, academic, and research purposes. Scraping Google Search results may conflict with their automated query policies. The developer assumes no liability for any misuse, rate-limiting, or terms of service violations caused by this tool. Use it with full respect for web ethics.

## 🚀 Architectural Evolution
Unlike the previous version which was constrained to Pinterest's specific DOM layout, this upgraded repository implements a fundamentally redesigned algorithm capable of navigating Google's search engine, locating original image sources, and resolving dynamic elements to extract full-resolution assets.

## 🧠 Algorithm Workflow
The core engine operates through the following systematic phases:
1. **Query Parsing & Formatting:** Normalizes raw user input string (e.g., `"cat with blue eyes"`) by splitting keywords and restructuring spaces into `+` operators to compile valid search engine URLs.
2. **Dynamic DOM Interaction:** Deploys automated browser actions to navigate the target Google Search query and triggers programmatic scrolling to dynamically load up to ~400 image nodes.
3. **Targeted Element Extraction:** Scans the rendering tree to identify and isolate specific image container box elements based on modern HTML class selectors.
4. **Asynchronous Source Resolution:** Iterates through individual nodes, simulates interaction, waits for high-resolution resource loaders to finish, and verifies HTTP status codes of the source URLs.
5. **Asset Pipeline:** Feeds validated URLs into a background downloading stream using the `requests` library, safely storing them into structurally organized local directories.

## 🛠️ Technical Implementation
- **Language:** Python 3.x
- **Key Modules:** Selenium WebDriver, Requests, Time/OS file management.
- **Output Capability:** Supports mass downloading of `JPEG`, `PNG`, and raw image formats with automated resolution upgrade fallback.

## 📄 License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
