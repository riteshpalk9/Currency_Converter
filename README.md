# React + Vite

# Currency Converter

![Currency Converter](https://via.placeholder.com/1200x500.png?text=Currency+Converter+App)

A fast and accurate currency converter built using **Vite + React** with **custom hooks** for efficient state management. Designed for **production-grade** performance and scalability.

## Features
- ⚡ Ultra-fast performance with Vite
- 🔄 Real-time exchange rates using an API
- 🎣 Custom hooks for API fetching and caching
- 🌍 Supports multiple currencies with live conversion
- 🎨 Modern UI with responsive design
- ✅ Error handling & loading states for smooth UX
- 📈 Optimized for production with best practices

## Tech Stack
- **Frontend**: React, Vite, TailwindCSS
- **State Management**: Custom hooks, Context API
- **API Integration**: [Exchange Rate API](https://exchangerate-api.com/)
- **Deployment**: Vercel / Netlify

## Installation & Setup

### Clone the repository
```sh
git clone https://github.com/riteshpalk9/Currency_converter.git
cd Currency_converter
```

### Install dependencies
```sh
npm install
```

### Run the development server
```sh
npm run dev
```

### Build for production
```sh
npm run build
```
## API Link (CDN)
This project uses the following API for fetching currency exchange rates:

🔗 [Currency API CDN](https://cdn.jsdelivr.net/npm/@fawazahmed0/currency-api@latest/v1/currencies/)

Example API endpoint:
```sh
https://cdn.jsdelivr.net/npm/@fawazahmed0/currency-api@2024-03-06/v1/currencies/usd.json
```

## Custom Hooks
This project utilizes custom hooks to manage API calls efficiently:

```js
// useCurrencyInfo.js
import { useEffect, useState } from "react";

function useCurrencyInfo(currency) {
  const [data, setData] = useState({});
  useEffect(() => {
    fetch(
      `https://cdn.jsdelivr.net/npm/@fawazahmed0/currency-api@2024-03-06/v1/currencies/${currency}.json`
    )
      .then((res) => res.json())
      .then((res) => setData(res[currency]));
    console.log(`Printing data ${data}`);
  }, [currency]);
  return data;
}

export default useCurrencyInfo;
```

## License
This project is **MIT Licensed**. Feel free to use and modify it!

## Contributing
Want to improve the project? Feel free to fork and submit a PR!

## Author
👨‍💻 **Ritesh Pal** 






