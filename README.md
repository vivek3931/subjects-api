# 📚 Subjects API (Static JSON)

Welcome to the **Subjects API** 🎓 — a free, static JSON dataset containing a wide collection of academic subjects, competitive exams, certifications, and specializations.  

This project is hosted using **GitHub Pages** 🌐 and can be accessed like a simple REST API endpoint (no server, no cold start 🚀).

---

## 🔗 Live URL
You can directly access the subjects data here:

👉 [https://vivek3931.github.io/subjects-api/subjects.json](https://vivek3931.github.io/subjects-api/subjects.json)

---

## 📂 Example Data
```json
[
  { "value": "Mathematics", "label": "Mathematics", "category": "STEM" },
  { "value": "Physics", "label": "Physics", "category": "STEM" },
  { "value": "Computer Science Engineering", "label": "Computer Science Engineering", "category": "Engineering" },
  { "value": "Medicine (MBBS)", "label": "Medicine (MBBS)", "category": "Medical Sciences" }
]
````

---

## 🛠️ Usage in JavaScript

```js
fetch("https://vivek3931.github.io/subjects-api/subjects.json")
  .then(response => response.json())
  .then(data => {
    console.log(data); // Array of subjects
  });
```

---

## 🛠️ Usage in React

```jsx
import { useEffect, useState } from "react";

export default function SubjectsList() {
  const [subjects, setSubjects] = useState([]);

  useEffect(() => {
    fetch("https://vivek3931.github.io/subjects-api/subjects.json")
      .then(res => res.json())
      .then(setSubjects);
  }, []);

  return (
    <ul>
      {subjects.map((sub, i) => (
        <li key={i}>
          {sub.label} ({sub.category})
        </li>
      ))}
    </ul>
  );
}
```

---

## 🌟 Features

* ✅ 300+ subjects across STEM, Humanities, Languages, Commerce, Medical, Engineering, and more
* ✅ Easy-to-use JSON format
* ✅ Always live with **GitHub Pages**
* ✅ Free & open-source

---

## 📌 Use Cases

* 📘 Educational platforms
* 🧑‍🏫 Online tutoring websites
* 🎯 Competitive exam preparation apps
* 📊 Data visualization or dropdowns in projects

---

## 🤝 Contributing

Want to add more subjects? Fork this repo and create a pull request.

---

## 📜 License

MIT License © 2025 [Vivek Singh](https://github.com/vivek3931)

```
