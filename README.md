# CineAnime starter (free MVP)

## इसमें क्या है
- Responsive Movie / Series / Anime catalogue
- Search, genre filters, title detail modal
- Favourite list (browser local storage)
- अधिकृत वीडियो URL के लिए HTML5 player placeholder
- PWA manifest + service worker (Android पर installable website)

## लोकल में चलाएँ
`index.html` को ब्राउज़र में खोलें। PWA install/service worker के लिए HTTPS hosting या localhost चाहिए।

## मुफ्त में वेबसाइट प्रकाशित करना
1. GitHub पर account बनाकर `cineanime` नाम का public repository बनाएँ।
2. इस ZIP की सभी फाइलें repository में upload करें।
3. Settings → Pages → Deploy from branch → `main` → `/ (root)` → Save चुनें।
4. कुछ मिनट बाद GitHub Pages URL खुलेगा।

## Android App की तरह install करना
1. Android Chrome में प्रकाशित HTTPS वेबसाइट खोलें।
2. Chrome menu (⋮) → Install app या Add to Home screen चुनें।
3. ऐप फोन की home screen पर दिखेगा। यह PWA है, Play Store APK नहीं।

## अपना content कैसे जोड़ें
`index.html` में `const items=[ ... ]` खोजें। हर item में:
- `title`: content का नाम
- `kind`: `movie`, `series`, या `anime`
- `genre`, `year`, `emoji`, `c1`, `c2`, `desc`
- `url`: अपने या लिखित अनुमति वाले MP4/HLS वीडियो का HTTPS URL

वीडियो फ़ाइलों को GitHub repository में upload न करें; free hosting की storage/bandwidth सीमाएँ होती हैं। वीडियो के लिए ऐसा host/CDN चुनें जिसके terms streaming की अनुमति देते हों। बाहरी HLS (`.m3u8`) playback के लिए कुछ browsers में अलग player library की जरूरत हो सकती है।

## महत्वपूर्ण सीमाएँ
यह शुरुआती front-end demo है, पूर्ण Netflix-जैसा backend नहीं। इसमें अभी admin login, server database, user accounts, subscriptions, multi-device sync, DRM, subtitles/episode management या licensed content feed नहीं है। इन सुविधाओं के लिए backend, database, authentication और content distribution सेवा जोड़नी होगी। किसी भी copyrighted movie/anime को बिना अधिकार stream या redistribute न करें।
