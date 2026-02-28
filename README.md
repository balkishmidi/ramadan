# 🌙 Ramadan Hub - Multilingual Edition

A beautiful, feature-rich web application with **3 languages** (English, Arabic, French), **dynamic prayer times** using Aladhan API, and **Tunisia as default location** with country selection.

## ✨ New Features

### 🌍 Multi-Language Support
- **English** - Full interface in English
- **العربية (Arabic)** - Complete RTL support with Arabic interface
- **Français (French)** - Full French translation
- Instant language switching with no page reload
- RTL (Right-to-Left) layout for Arabic

### 🕌 Enhanced Prayer Times
- **Tunisia as Default Location** 🇹🇳
- **Dynamic Country Selection** - Choose from 25+ countries
- **Real-time Prayer Times** - Powered by Aladhan API
- **Next Prayer Countdown** - Live countdown to next prayer
- **Highlighted Next Prayer** - Visual indicator of upcoming prayer
- **Accurate Timings** - Based on Islamic calculations

### 🎯 Dynamic Features
- **Live Countdown Timer** - Updates every second
- **Automatic Next Prayer Detection** - Always shows what's next
- **Country-Specific Timings** - Accurate for each location
- **12-Hour Time Format** - Easy to read AM/PM display

## 🌟 All Original Features Included

1. **🕌 Prayer Times** with country selection
2. **📿 Digital Tasbih** with haptic feedback
3. **🍽️ Recipe Randomizer** with 30+ recipes
4. **💡 Daily Sunnah Tips** (translated in all languages)
5. **💰 Zakat Calculator** (multi-language)

## 🚀 Quick Start

Simply open `index.html` in your browser - no installation needed!

```bash
# Open directly
open index.html

# Or use a local server
python -m http.server 8000
# Then visit: http://localhost:8000
```

## 🌐 Supported Countries

The app includes 25+ countries with accurate prayer times:

### Middle East & North Africa
- 🇹🇳 Tunisia (Default)
- 🇸🇦 Saudi Arabia
- 🇦🇪 United Arab Emirates
- 🇪🇬 Egypt
- 🇲🇦 Morocco
- 🇩🇿 Algeria
- 🇮🇶 Iraq
- 🇯🇴 Jordan
- 🇰🇼 Kuwait
- 🇱🇧 Lebanon
- 🇱🇾 Libya
- 🇴🇲 Oman
- 🇵🇸 Palestine
- 🇶🇦 Qatar
- 🇸🇩 Sudan
- 🇸🇾 Syria
- 🇾🇪 Yemen

### Asia
- 🇹🇷 Turkey
- 🇵🇰 Pakistan
- 🇲🇾 Malaysia
- 🇮🇩 Indonesia

### Western Countries
- 🇬🇧 United Kingdom
- 🇺🇸 United States
- 🇨🇦 Canada
- 🇫🇷 France
- 🇩🇪 Germany

## 📖 How to Use

### Changing Language
1. Click on the language buttons at the top-right
2. Choose: **English** | **العربية** | **Français**
3. Interface updates instantly

### Selecting Country
1. Go to Prayer Times section
2. Click the dropdown menu
3. Select your country
4. Prayer times update automatically

### Understanding Prayer Times Display
- **Golden Banner** - Shows next prayer with countdown
- **Highlighted Card** - Next prayer has gold border and glow
- **Live Updates** - Countdown refreshes every second
- **12-Hour Format** - Easy to read (e.g., 5:30 AM)

## 🔧 Technical Details

### API Integration
```javascript
// Aladhan API for accurate prayer times
const api = 'https://api.aladhan.com/v1/timingsByCity';
const params = {
    city: 'Tunis',
    country: selectedCountry,
    method: 2  // Islamic Society of North America (ISNA)
};
```

### Language Structure
```javascript
const translations = {
    en: { /* English translations */ },
    ar: { /* Arabic translations */ },
    fr: { /* French translations */ }
};
```

### RTL Support
- Automatic direction change for Arabic
- Mirrored layout elements
- Right-aligned text
- Proper font selection (Scheherazade New for Arabic)

## 🎨 Design Features

### Arabic-Specific Design
- **Scheherazade New** font for beautiful Arabic text
- RTL layout with mirrored components
- Proper text alignment
- Arabic numerals support

### Prayer Times Display
- **Next Prayer Banner** - Golden gradient highlight
- **Pulsing Animation** - Draws attention to next prayer
- **Live Countdown** - Shows hours and minutes remaining
- **Visual Indicators** - Icons for each prayer time

## 📱 Responsive Design

- Mobile-first approach
- Touch-friendly interface
- Optimized for all screen sizes
- Language selector adapts to RTL

## 🌙 Prayer Time Accuracy

The app uses the **Aladhan API** which provides:
- Accurate calculations based on Islamic methods
- Timezone-aware results
- Location-specific adjustments
- Multiple calculation methods (using ISNA method)

### Prayer Names in All Languages

| Prayer | English | Arabic | French |
|--------|---------|--------|--------|
| Pre-dawn | Fajr | الفجر | Fajr |
| Noon | Dhuhr | الظهر | Dhuhr |
| Afternoon | Asr | العصر | Asr |
| Sunset | Maghrib | المغرب | Maghrib |
| Night | Isha | العشاء | Isha |

## 🔄 How Next Prayer Detection Works

```javascript
1. Get current time in minutes (e.g., 14:30 = 870 minutes)
2. Get all prayer times in minutes
3. Find first prayer time > current time
4. Calculate difference
5. Display countdown
6. Highlight that prayer card
7. Update every second
```

## 🌟 Features by Language

### All Features Fully Translated:
- ✅ Navigation menu
- ✅ Prayer time names
- ✅ Button labels
- ✅ Form labels
- ✅ Messages and notifications
- ✅ Daily tips
- ✅ Recipe instructions
- ✅ Calculator labels

## 📊 Browser Compatibility

- ✅ Chrome 90+
- ✅ Firefox 88+
- ✅ Safari 14+
- ✅ Edge 90+
- ✅ Mobile browsers (iOS Safari, Chrome Mobile)

## 🔐 Privacy & Offline

- No user data collection
- Works offline (after first load)
- localStorage only for Tasbih count
- API calls only for prayer times

## 🎯 Default Settings

- **Language**: English
- **Country**: Tunisia 🇹🇳
- **Direction**: LTR (switches to RTL for Arabic)
- **Time Format**: 12-hour with AM/PM

## 🛠️ Customization

### Change Default Country
Edit line in HTML:
```html
<option value="TN" selected>Tunisia</option>
<!-- Change "TN" to your preferred country code -->
```

### Add More Countries
Add to the select dropdown:
```html
<option value="XX">Your Country</option>
```

### Modify Calculation Method
Change method parameter in API call:
```javascript
method: 2  // 2 = ISNA, 3 = MWL, 4 = Makkah, etc.
```

## 📖 Translation Keys

To add a new translation:
```javascript
translations.newLang = {
    title: "Your Translation",
    subtitle: "Your Subtitle",
    // ... add all keys
};
```

## 🎨 Color Scheme

```css
--gold: #D4AF37;          /* Primary accent */
--dark-purple: #2D1B4E;   /* Background */
--cream: #FFF8E7;         /* Text */
--soft-gold: #F4E4C1;     /* Secondary accent */
```

## 🤝 Contributing

To improve translations or add features:
1. Edit the translations object
2. Test in all 3 languages
3. Ensure RTL works properly for Arabic
4. Check responsive design

## 🌙 Ramadan Mubarak!

Built with ❤️ for the global Muslim community

---

## 📞 Support

### Common Issues

**Prayer times not loading?**
- Check internet connection
- Verify country code is valid
- API might be temporarily down

**Arabic text not displaying correctly?**
- Browser must support RTL
- Font might not be loaded
- Clear cache and reload

**Countdown not updating?**
- JavaScript must be enabled
- Check browser console for errors
- Refresh the page

**Language not switching?**
- Clear browser cache
- Check JavaScript console
- Ensure all translation keys exist

---

### API Documentation

**Aladhan API**: https://aladhan.com/prayer-times-api

**Endpoints Used**:
- `/v1/timingsByCity` - Get prayer times by city/country
- Method 2 (ISNA) for calculations
- Automatic timezone detection

---

## 🎁 Future Enhancements

- [ ] Add more languages (Urdu, Turkish, Indonesian)
- [ ] Offline mode with cached prayer times
- [ ] Custom calculation method selection
- [ ] Qibla direction finder
- [ ] Prayer time notifications
- [ ] Monthly prayer calendar
- [ ] Mosque finder by location

---

**Version**: 2.0 (Multilingual with Dynamic Prayer Times)
**Last Updated**: 2026
**License**: Open Source
