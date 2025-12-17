<div align="center">
<img width="1200" height="475" alt="La Sirena Banner" src="https://github.com/user-attachments/assets/0aa67016-6eaf-458a-adb2-6e31a0763ed6" />
</div>

# La Sirena - Virtual Stylist & Runway

**AI-Powered Fashion Try-On Application**

Transform your fashion vision into reality with cutting-edge AI technology. Upload a photo, select clothing items, and generate professional lookbooks with multiple poses.

## ✨ Features

- 🎨 **Virtual Try-On**: Dress any person with different clothing items using AI
- 🤖 **Multiple AI Models**:
  - **Gemini 3 Pro Image** - Google's latest image generation model
  - **SeeDream V4.5** - Advanced try-on technology
  - **Flux 2 Pro** - High-quality image transformation
- 📸 **Lookbook Generation**: Create 4 professional poses automatically
  - Frontal pose
  - 3/4 view
  - Profile view  
  - Dynamic movement
- 🎬 **Runway Videos**: Generate fashion runway videos with Veo 3.1
- 👔 **Custom Wardrobe**: Upload and manage your own clothing collection
- 🖼️ **Professional Output**: 2x2 grid layouts with elegant styling

## 🚀 Quick Start

### Prerequisites

- Node.js (v16 or higher)
- API Keys (see Configuration section)

### Installation

1. Clone the repository:
```bash
git clone https://github.com/joelGuerraArias/lasirena.git
cd lasirena
```

2. Install dependencies:
```bash
npm install
```

3. Configure your API keys (see Configuration section below)

4. Run the development server:
```bash
npm run dev
```

5. Open http://localhost:3000 in your browser

## ⚙️ Configuration

### API Keys Setup

You have two options to configure your API keys:

#### Option 1: Local JSON File (Recommended for Development)

1. Copy the example config file:
```bash
cp config.example.json config.json
```

2. Edit `config.json` and add your API keys:
```json
{
  "gemini_api_key": "YOUR_GEMINI_API_KEY_HERE",
  "wavespeed_api_key": "YOUR_WAVESPEED_API_KEY_HERE"
}
```

**Note**: The `config.json` file is ignored by git for security.

#### Option 2: Through the UI

1. Click the "Configure API Key" button in the app header
2. Enter your API key
3. Keys are stored in browser localStorage

### Getting API Keys

**Gemini API Key** (for Gemini 3 Pro):
1. Visit [Google AI Studio](https://aistudio.google.com/app/apikey)
2. Sign in with your Google account
3. Click "Create API Key"
4. Copy your key

**Wavespeed API Key** (for SeeDream/Flux):
1. Visit [Wavespeed.ai](https://wavespeed.ai)
2. Create an account or sign in
3. Go to API Keys in your dashboard
4. Copy your key

## 🎯 How to Use

1. **Upload a Person's Photo**: Click "The Muse" section and upload a photo
2. **Select Clothing**: Choose items from the wardrobe:
   - Top (shirts, dresses, coats)
   - Bottom (pants, skirts, shorts)
   - Footwear (shoes, boots)
3. **Choose AI Model**: Select Gemini, SeeDream, or Flux
4. **Generate Lookbook**: Click "Generate Lookbook" to create 4 poses
5. **Optional**: Generate a runway video from your favorite look

## 🛠️ Tech Stack

- **Frontend**: React 19 + TypeScript
- **Build Tool**: Vite 6
- **Styling**: Tailwind CSS (utility-first)
- **AI Services**:
  - Google Gemini API (@google/genai)
  - Wavespeed API (SeeDream & Flux)
  - Veo 3.1 (video generation)

## 📁 Project Structure

```
la-sirena/
├── components/          # React components
│   └── UploadZone.tsx  # File upload interface
├── services/           # API integrations
│   ├── configService.ts   # Configuration management
│   ├── geminiService.ts   # Gemini AI integration
│   └── seedreamService.ts # SeeDream/Flux integration
├── public/
│   └── clothes/        # Sample clothing images
├── App.tsx             # Main application component
├── types.ts            # TypeScript type definitions
├── utils.ts            # Utility functions
├── config.json         # API keys (not in git)
└── config.example.json # Example configuration

```

## 🎨 Features in Detail

### Virtual Try-On
The app uses advanced AI to realistically dress a person with selected clothing items while maintaining:
- Original person's facial features and body proportions
- Consistent framing across all poses
- Professional studio lighting and white background
- Full body visibility from head to toe

### Lookbook Generation
Creates a professional 2x2 grid with:
- 4 different poses of the same outfit
- Elegant labels and styling
- High-resolution output
- Download options for grid and individual poses

### Custom Wardrobe
- Upload your own clothing items
- Organize by category (tops, bottoms, footwear)
- Delete items you no longer need
- Persistent storage in browser

## 📝 Scripts

```bash
npm run dev      # Start development server (port 3000)
npm run build    # Build for production
npm run preview  # Preview production build
```

## 🔒 Security

- API keys in `config.json` are **never** committed to git
- Keys stored in localStorage remain in the browser only
- All API calls are made from the client side
- No backend server required

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## 📄 License

This project is private and proprietary.

## 👨‍💻 Author

Joel Guerra Arias
- GitHub: [@joelGuerraArias](https://github.com/joelGuerraArias)

## 🙏 Acknowledgments

- Google AI Studio for Gemini API
- Wavespeed.ai for SeeDream and Flux APIs
- Sample clothing images from public domain

---

Made with ❤️ using AI Technology
