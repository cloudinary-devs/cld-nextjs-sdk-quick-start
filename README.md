# Cloudinary Next.js SDK Quick Start

A quick start sample project demonstrating how to integrate Cloudinary's image and video management capabilities into a Next.js application using the `next-cloudinary` SDK.

## Features

- 🖼️ Image upload with Cloudinary Upload Widget
- 🎨 On-the-fly image transformations
- ⚡ Optimized image delivery
- 🔧 TypeScript support

## Prerequisites

- Node.js 22 or later
- This project uses `next-cloudinary` version 7, which requires Next.js 16 or later and React 18.2 or 19
- A Cloudinary account ([sign up for free](https://cloudinary.com/users/register/free))
- Your Cloudinary credentials:
  - Cloud Name
  - Upload Preset (unsigned)

## Setup

1. **Clone the repository**

```bash
git clone <repository-url>
cd cld-nextjs-sdk-quick-start
```

2. **Install dependencies**

```bash
npm install
```

3. **Configure environment variables**

Create a `.env.local` file in the root directory:

```bash
NEXT_PUBLIC_CLOUDINARY_CLOUD_NAME=your_cloud_name
```

Replace `your_cloud_name` with your actual Cloudinary cloud name from your [Cloudinary Console](https://console.cloudinary.com/).

4. **Create an Upload Preset**

- Go to your [Cloudinary Console](https://console.cloudinary.com/)
- Navigate to Settings → Upload
- Scroll to "Upload presets" and click "Add upload preset"
- Set the signing mode to "Unsigned"
- Save the preset and note the preset name
- Update the `uploadPreset` value in `app/page.tsx` with your preset name

## Running the Project

Start the development server:

```bash
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) in your browser.

## Project Structure

```
cld-nextjs-sdk-quick-start/
├── app/
│   ├── page.tsx          # Main upload demo page
│   └── layout.tsx        # Root layout
├── .env.local            # Environment variables (not in git)
├── next.config.ts        # Next.js configuration
└── package.json          # Dependencies
```

## What's Included

### Image Upload (`app/page.tsx`)

- Uses `CldUploadButton` component for easy file uploads
- Handles upload success with TypeScript type safety
- Displays uploaded image information

### Image Transformation

- Uses `CldImage` component for optimized delivery
- Demonstrates crop transformation (`crop="fill"`)
- Automatic format and quality optimization

## Learn More

### Cloudinary Resources

- [Cloudinary Documentation](https://cloudinary.com/documentation)
- [Cloudinary Next.js SDK Documentation](https://cloudinary.com/documentation/nextjs_integration)

### Next.js Resources

- [Next.js Documentation](https://nextjs.org/docs)
- [Learn Next.js](https://nextjs.org/learn)

## Common Issues

### Upload Widget Not Opening

- Verify your cloud name is correct in `.env.local`
- Ensure your upload preset is set to "unsigned"
- Check browser console for errors

### Images Not Displaying

- Confirm the public ID is correct
- Verify your cloud name is properly configured
- Check that the image was successfully uploaded to Cloudinary

## Next Steps

Explore more Cloudinary features:

- Video upload and transformation
- AI-powered image enhancements
- Responsive images with automatic breakpoints
- Advanced transformations (filters, effects, overlays)
- Media library integration


