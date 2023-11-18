# Python-Codes

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>My Project</title>
  <style>
    .tab {
      display: none;
    }

    .tabset {
      margin-bottom: 20px;
    }

    .tabset .tab-label {
      display: inline-block;
      padding: 10px;
      border: 1px solid #ccc;
      cursor: pointer;
    }

    .tabset .tab-label.active {
      background-color: #eee;
    }
  </style>
</head>
<body>
  <h1>My Project</h1>

  <div class="tabset">
    <div class="tab-label active" onclick="showTab('python')">Python</div>
    <div class="tab-label" onclick="showTab('javascript')">JavaScript</div>
  </div>

  <div id="python-tab" class="tab">
    <h2>Python Example</h2>

    <pre>
      print("Hello, world!")
    </pre>
  </div>

  <div id="javascript-tab" class="tab">
    <h2>JavaScript Example</h2>

    <pre>
      console.log("Hello, world!");
    </pre>
  </div>

  <script>
    function showTab(tabName) {
      var tabs = document.querySelectorAll('.tab');
      for (var i = 0; i < tabs.length; i++) {
        tabs[i].style.display = 'none';
      }

      var tab = document.getElementById(tabName + '-tab');
      tab.style.display = 'block';

      var tabLabels = document.querySelectorAll('.tab-label');
      for (var i = 0; i < tabLabels.length; i++) {
        tabLabels[i].classList.remove('active');
      }

      var tabLabel = document.querySelector('.tab-label[onclick="showTab(\'' + tabName + '\')"]');
      tabLabel.classList.add('active');
    }
  </script>
</body>
</html>
