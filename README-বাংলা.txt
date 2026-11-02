# BM Fixer — ফ্রি PWA প্যাকেজ

এই প্যাকেজটি BM Fixer-কে Android Chrome থেকে ইনস্টলযোগ্য অ্যাপের মতো চালানোর জন্য প্রস্তুত। এতে কোনো পেইড সার্ভিস যুক্ত নেই।

## গুরুত্বপূর্ণ
- PWA ইনস্টল করতে ওয়েবসাইটটি HTTPS-এ প্রকাশ করতে হবে। শুধু ফোনে HTML ফাইল খুললে Service Worker/PWA ইনস্টল কাজ করবে না।
- বিনামূল্যে GitHub Pages ব্যবহার করা যায়; GitHub অ্যাকাউন্ট ও একবার ফাইল আপলোড/সেটআপ দরকার।
- Supabase Sync করতে ইন্টারনেট লাগবে। অফলাইনে অ্যাপের shell খোলা যেতে পারে, কিন্তু ক্লাউড Sync হবে না।
- Supabase-এর Public Anon/Publishable key-ই ব্যবহার করবেন; Secret বা service_role key কখনো index.html-এ দেবেন না।
- এই প্যাকেজে Supabase ডাটাবেস, Auth বা RLS নীতি পরিবর্তন করা হয়নি।

## GitHub Pages-এ ফ্রি প্রকাশ
1. GitHub-এ সাইন ইন করে নতুন Public repository তৈরি করুন, যেমন `bm-fixer-app`।
2. এই ZIP-এর ভেতরের সব ফাইল ও `icons` ফোল্ডার repository-র মূল জায়গায় আপলোড করুন। `index.html` যেন root-এ থাকে।
3. Repository → Settings → Pages খুলুন। `Deploy from a branch` নির্বাচন করুন, Branch `main`, folder `/ (root)` দিয়ে Save করুন।
4. GitHub যে HTTPS ওয়েব ঠিকানা দেবে, সেটি Chrome-এ খুলুন। প্রথমবার লোড হতে কয়েক মিনিট লাগতে পারে।
5. Android Chrome-এর তিন ডট মেনু → `Install app` বা `Add to Home screen` চাপুন।

## আপডেট
পরবর্তীতে অ্যাপের HTML বদলালে নতুন `index.html` একই repository-তে আপলোড করুন। Service worker cache version বদলাতে হলে `sw.js`-এর `bm-fixer-shell-v1` নামটি `v2` করুন।
