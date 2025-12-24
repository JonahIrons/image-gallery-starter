# Next.js Image Gallery with Cloudinary Analysis
This project is based on the [Next.js Image Gallery Starter](https://vercel.com/templates/next.js/image-gallery-starter) from Vercel. It is a modern image gallery built with Next.js, Tailwind CSS, and Cloudinary.

## New Feature: Face Count Filtering
I implemented a dynamic filtering system that organizes images based on the number of people detected in the photo.

### Filtering options:
- All images
- No people (0 faces)
- Solo (1 face)
- Groups (2+ faces)

## Technical Implementation
- **Cloudinary Image Analysis:** The app takes advantage of Cloudinary's `face_count` metadata (accessed via the Admin API) to determine the composition of each image.
- **State Management:** I utilized React useState to manage the active filter criteria.
- **Client-Side Filtering:** The gallery re-renders the image grid in real-time without requiring a page reload or additional API calls, ensuring a clean user experience.

## Setup & Installation
Clone the repo:
```
git clone https://github.com/JonahIrons/image-gallery-starter
```

Install dependencies:
```
npm install
```

Set up Environment Variables: Create a .env.local file in the root directory and add your Cloudinary credentials:
```
NEXT_PUBLIC_CLOUDINARY_CLOUD_NAME=...
CLOUDINARY_API_KEY=...
CLOUDINARY_API_SECRET=...
CLOUDINARY_FOLDER=...
```

Run the development server:
```
npm run dev
```
