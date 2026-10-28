TEAM Z — GitHub Pages + PWA Demo

এই ZIP-এ GitHub Pages-এ host করার জন্য static PWA setup যোগ করা হয়েছে:
- manifest.webmanifest
- sw.js (basic offline cache)
- icons/icon-192.png এবং icon-512.png
- index.html-এ PWA manifest ও service worker registration

GitHub Pages-এ চালু করার ধাপ:
1. GitHub.com-এ sign in করুন।
2. New repository তৈরি করুন; নাম দিতে পারেন team-z-app।
3. এই ZIP Extract করুন।
4. Extract করা TEAMZ_Full_App_Demo ফোল্ডারের ভেতরের সব ফাইল/ফোল্ডার repository-র ROOT-এ upload করুন। অর্থাৎ index.html যেন repository-র root-এ থাকে; পুরো parent folder-টি আবার upload করবেন না।
5. Commit changes করুন।
6. Repository → Settings → Pages খুলুন।
7. Build and deployment-এ "Deploy from a branch" বেছে নিন।
8. Branch হিসেবে main এবং folder হিসেবে /(root) বেছে Save করুন।
9. কিছুক্ষণ পর GitHub Pages URL দেখাবে; সেটি HTTPS-এ খুলুন।
10. Android Chrome-এ URL খুলে browser menu (⋮) → Install app / Add to Home screen চাপুন। iPhone-এ Safari → Share → Add to Home Screen।

গুরুত্বপূর্ণ:
- GitHub Pages static hosting; এটি নিজে database বা secure login backend নয়।
- এই demo-র registration/profile/program data localStorage-এ থাকে, তাই প্রতিটি browser/device আলাদা data রাখে।
- Demo admin login নিরাপদ authentication নয়। Public production app-এর আগে Supabase/Firebase/backend, real auth, database rules/RLS এবং admin authorization লাগবে।
- PWA/offline cache নতুন version deploy করার পর update হতে একটু সময় নিতে পারে; browser refresh করুন, দরকার হলে site data/cache clear করুন।
- Local file হিসেবে index.html double-click করলে service worker/PWA install সাধারণত কাজ করবে না; HTTPS GitHub Pages URL ব্যবহার করুন।
