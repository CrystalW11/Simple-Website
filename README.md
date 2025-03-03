<img width="606" alt="image" src="https://github.com/user-attachments/assets/4ef99c53-2eec-46f2-ba52-6be310ecd135" /><img width="606" alt="image" src="https://github.com/user-attachments/assets/a5071474-d605-4295-bcbb-b4e8b02770aa" /># Simple-Website

<img width="478" alt="image" src="https://github.com/user-attachments/assets/70d9acf7-b817-4b94-b900-df52aa32e699" />
<img width="479" alt="image" src="https://github.com/user-attachments/assets/61b331f6-8419-49a9-bfef-17ea8abb06f5" />

### `index.html`
```
<!DOCTYPE html>
<html lang="en">
<head>
     <meta charset="UTF-8">
     <meta http-equiv="X-UA-Compatible" content="IE=edge">
     <meta name="viewport" content="width=device-width, initial-scale=1.0">
     <title>Simple Website</title>
     <link rel="stylesheet" href="main.css">
</head>
<body class="light-theme">
     <h1>Task List</h1>
     <p id="msg">Current Tasks:</p>
     <ul>
          <li class="list">Add visual styles</li>
          <li class="list">Add light and dark themes</li>
          <li>Enable Switching the theme</li>
     </ul>
     <div>
          <button class="btn">Dark</button>
     </div>
     <script src="app.js"></script>
     <noscript>You need to enable JavaScript to view the full site.</noscript>
</body>
</html>
```

<img width="855" alt="image" src="https://github.com/user-attachments/assets/674b92ea-b982-4761-8c39-ec5226ad9aab" />

### `app.js`

```
'use strict';

const switcher = document.querySelector('.btn');

switcher.addEventListener('click', function () {
  document.body.classList.toggle('light-theme');
  document.body.classList.toggle('dark-theme');

  const className = document.body.className;
  if (className == "light-theme") {
    this.textContent = "Dark";
  } else {
    this.textContent = "light";
  }

  console.log('current class name: ' + className);
});
```


<img width="606" alt="image" src="https://github.com/user-attachments/assets/4e76eba3-7dbc-4579-b984-62265e5a350b" />

### `main.css`

```
:root {
     --green: #00FF00;
     --white: #FFFFFF;
     --black: #000000;
}

body {
     background: var(--bg);
     color: var(--fontColor);
     font-family: helvetica;
}

li {
     list-style: circle;
}

.list {
     list-style: square;
}

.light-theme {
     --bg: var(--green);
     --fontColor: var(--black);
     --btnBg: var(--black);
     --btnFontColor: var(--white);
}

.dark-theme {
     --bg: var(--black);
     --fontColor: var(--green);
     --btnBg: var(--white);
     --btnFontColor: var(--black);
}

.btn {
     position: absolute;
     top: 20px;
     left:250px;
     height: 50px;
     width: 50px;
     border-radius: 50%;
     border: none;
     color:var(--btnFontColor);
     background-color: var(--btnBg);
}
```



<img width="629" alt="image" src="https://github.com/user-attachments/assets/a2b223ea-61e8-4661-aec6-a3450ad6862c" />


