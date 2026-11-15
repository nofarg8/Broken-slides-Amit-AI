# המצגת השבורה - פולאריס, שיעור 6

רכיב אינטראקטיבי לשיעור 6 בקורס מיומנויות בינה מלאכותית: "יוצרים מצגת ובוחנים את השפעת הגדרת קהל היעד".
התלמידים בודקים את המצגת של רובי, מוצאים 7 תקלות, ומגלים אילו מהן נבעו מפרומפט חסר.

הרכיב הוא קובץ `index.html` יחיד, בלי ספריות ובלי תלויות חיצוניות.

## העלאה ל-GitHub

המאגר: https://github.com/nofarg8/Broken-slides-Amit-AI

1. נכנסים לעמוד המאגר.
2. לוחצים על Add file ואחר כך על Upload files (במאגר ריק: uploading an existing file).
3. גוררים את `index.html` ואת `README.md`, ולוחצים על Commit changes.

## הפעלת GitHub Pages

1. במאגר נכנסים ל-Settings ואחר כך ל-Pages.
2. תחת Build and deployment בוחרים Source: Deploy from a branch.
3. בוחרים Branch: `main` ותיקייה `/ (root)`, ולוחצים על Save.
4. אחרי דקה או שתיים הרכיב זמין בכתובת https://nofarg8.github.io/Broken-slides-Amit-AI/

## הטמעה בשיעור

```html
<iframe src="https://nofarg8.github.io/Broken-slides-Amit-AI/" width="100%" height="680" style="border:0" allow="autoplay"></iframe>
```

בהעלאה למאגר אחר מחליפים את הכתובת לפי התבנית `https://USERNAME.github.io/REPO/`.

כדי שכפתור ההעתקה של קוד הסיום יעבוד בכל הדפדפנים, אפשר להוסיף הרשאת לוח: `allow="autoplay; clipboard-write"`. גם בלי ההרשאה יש לרכיב דרך העתקה חלופית, והקוד ניתן לסימון ידני.

## סיום הפעילות

- קוד הסיום מוגדר בקבוע בראש הסקריפט: `const COMPLETION_CODE = 'בודק-פולאריס';`
- במעבר למסך הסיום נשלחת לחלון האב ההודעה:

```js
window.parent.postMessage({type:'polaris-complete', lesson:6, activity:'broken-deck'}, '*');
```

## התאמת עיצוב

כל הצבעים מוגדרים כמשתני CSS בבלוק `:root` בראש הקובץ (`--bg`, `--accent`, `--ok`, `--warn` ועוד). כדי להתאים לעיצוב הקורס מספיק לשנות אותם שם.

## התאמת תוכן

כל הטקסטים נמצאים באובייקטים בראש הסקריפט: `MODALS` (הנוהל והפרומפט), `FAULTS` (רמזים, אפשרויות, הסברים ושורות הצ'קליסט), `LINES` (כרטיסי השורות של שלב 2) ו-`SLIDES` (תוכן השקפים).
