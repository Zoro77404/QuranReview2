# مراجعة تبارك وعمّ 🐥

لعبة لمراجعة حفظ جزء تبارك وجزء عمّ (من سورة الملك إلى سورة الناس).

> **نسخة التجربة** — فيها 🎤 والخريطة: https://zoro77404.github.io/QuranReview2/
>
> النسخة الأساسية (بدون 🎤): https://zoro77404.github.io/QuranReview/

- 🗺️ خريطة رحلة من الملك إلى الناس: كل سورة جزيرة، وفيها ٣ نجوم ⭐ حسب أفضل نتيجة.
- 🎤 اضغطي المايك واقرئي: التطبيق يسمعك ويلوّن الكلمات (أخضر صح، أحمر غلط، رمادي ناقص). ٩٠٪ أو أكثر = نجمة واحتفال.
  أول مرة يتنزّل «المستمع» (نموذج ترتيل whisper-tiny-ar-quran)، وبعدها يشتغل من الجوال نفسه بدون إنترنت.
- 🥚→🐣→🐥→🐤→🦅 صاحبتك تكبر كل ما زادت النجوم، و🔥 تعدّ الأيام اللي راجعتي فيها ورا بعض.
- كل التقدم محفوظ في المتصفح نفسه.

---

## For the developer

- **Test copy.** Hosted on GitHub Pages at https://zoro77404.github.io/QuranReview2/ (public repo).
  The main live site is the separate repo
  [Zoro77404/QuranReview](https://github.com/Zoro77404/QuranReview) (`Desktop\QuranReview`), currently on the version without 🎤 / map.
- Same origin as the live site, so caches use their own `quran-review2-` prefix and the app is named «تجربة».
- This folder must **never push to the live repo** — `origin` is QuranReview2 and a `pre-push` hook blocks the live URL.
- Run locally: `python -m http.server 8000` in this folder, then open http://localhost:8000/ (the mic needs localhost or https).
- To ship later: copy the changed files into `Desktop\QuranReview`, bump `CACHE` in `sw.js` there above `quran-review-v4`, and push from there.
- Code map and tuning notes: see `PROGRESS.md`.
