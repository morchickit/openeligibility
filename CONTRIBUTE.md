# תהליך עדכון הטקסונומיה

לאחר שהתקבלה החלטה על עדכון הטקסונומיה, יש לייצר גירסא חדשה שלה כאן.

1. כל השינויים המוצעים יבוצעו במסגרת Pull Request ל-Repository הזה.
2. יש להוסיף תיאור קצר של השינויים שבוצעו.
3. ב-Pull Request יש לשנות רק את הקבצים הבאים:

**הקובץ taxonomy.simple.yaml**

זה קובץ המקור של הטקסונומיה, בו ניתן לעשות שינויים. יש לשים לב לשמור על הפורמט של קובץ ה-YAML ולהקפיד על האינדנטציה הנכונה.
    
**הקובץ VERSION**

- זו הגירסא של הטקסונומיה לאחר השינויים.
- הגירסא של הטקסונומיה פועלת לפי העקרונות של גרסאות סמנטיות (semver.org).
- אם לא בטוחים מה צריכה להיותר הגירסא הבאה, תהליך ה-CI יוודא זאת במקומכם.
    
**הקובץ versions/renames.txt**

אם השינוי הנוכחי כולל שינויי שם של ערכים בטקסונומיה, יש למלא את הקובץ הזה בתיעוד השינויים הללו.

4. לאחר יצירת ה-Pull Request, יש לוודא שה-build שלו עובר בהצלחה. אם יש שגיאות, יש לתקן ולנסות שוב.
5. אם כל השינוי הוא רק בתרגומים, יש לייצר Pull Request עם שינוי בודד בקובץ VERSION (הכולל הקפצת גירסת ה-patch)