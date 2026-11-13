ARBIT — প্রাথমিক মোবাইল ওয়েব অ্যাপ প্রোটোটাইপ

চালানো:
1. ফাইলগুলো একটি HTTPS static hosting-এ আপলোড করুন (যেমন GitHub Pages/Netlify)।
2. Android Chrome-এ URL খুলে ⋮ > Add to Home screen / Install app নির্বাচন করুন।
3. অফলাইনে প্রথমবার লোড হওয়ার পর ব্যবহার করা যাবে।

বর্তমান ফিচার:
- Personal quick expense: সিগারেট, বাজার, যাতায়াত, চা; ক্যাটাগরি যোগ/সরানো
- Business basic sales/expense/capital/due entry
- Job basic expense/sales/allowance entry এবং RADT calculator
- Light/Dark theme
- Local browser storage
- JSON backup/restore, CSV export (Excel-এ খোলা যায়), Print to PDF

গুরুত্বপূর্ণ সীমাবদ্ধতা:
- এটি প্রাথমিক prototype; ডেটা শুধু এই ব্রাউজারের localStorage-এ থাকে।
- Google login, Firebase/Cloud sync, Google Drive backup, production-grade authentication/encryption এখনো যুক্ত নয়।
- এই প্রোটোটাইপে বাস্তব সংবেদনশীল আর্থিক তথ্য রাখার আগে Cloud backend ও নিরাপত্তা ব্যবস্থা তৈরি করতে হবে।
- Excel export CSV; প্রকৃত .xlsx ফরম্যাট পরবর্তী সংস্করণে যোগ করতে হবে।
- Kalpurush font ডিভাইসে ইনস্টল না থাকলে সিস্টেম Bengali fallback font ব্যবহার করবে। Font file সরবরাহ করলে embed করা যাবে।
