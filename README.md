# Bronify - Static Site Edition

Bronify is a music streaming app themed around LeBron James parody songs. This repository contains a static version of the application optimized for minimal to no hosting costs while maintaining all the functionality of the original app.

## Features

- Fully static site with no server-side rendering
- Progressive Web App (PWA) support with offline functionality
- Client-side routing that works with static hosting
- Media playback for audio and video content
- Custom media player with playlist support
- Mobile-friendly responsive design

## Prerequisites

- Node.js (v16 or higher)
- npm or yarn
- Basic knowledge of web hosting

## Setup and Installation

1. Clone this repository:
```bash
git clone https://github.com/your-username/lebronify.git
cd lebronify
```

2. Install dependencies:
```bash
npm install
```

3. Set up UI components:
```bash
npm run build
```

## Media Assets

**IMPORTANT**: Before using this application, you need to add your own media assets:

1. Create an `/assets` directory in the `/public` folder with the following structure:
```
/public/assets/
  /album-covers/     # Album artwork images
  /audio/            # MP3 files organized by album
  /images/           # Other images used in the app
  /thumbnails/       # Video thumbnails
  /videos/           # Video files
```

2. Update the media references in the data files:
- The main data files are located in `/lib/data.ts` and `/lib/artist-data.ts`
- All media URLs in these files are placeholders that need to be replaced with your actual media paths

## Development

Run the development server:

```bash
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

## Building and Deployment

### Building the Static Site

To build the static site:

```bash
npm run build
```

This will generate a static site in the `out` directory that can be deployed to any static hosting service.

### Deployment Options

#### Option 1: GitHub Pages

1. Set up a GitHub repository for your project.
2. Create a `.github/workflows/deploy.yml` file to automate deployment.
3. Push your changes to GitHub and the static site will be deployed automatically.

#### Option 2: Cloudflare Pages

1. Connect your GitHub repository to Cloudflare Pages.
2. Set the build command to `npm run build`.
3. Set the build output directory to `out`.

#### Option 3: Vercel Static Hosting

1. Import your project into Vercel.
2. Vercel will automatically detect the Next.js project and build it correctly.

## Customization

- Modify `/lib/data.ts` to add or update songs and playlists
- Modify `/app/globals.css` to change the styling
- Add your own media files to the `/public/assets` directory

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is open-source and available under the MIT License.

