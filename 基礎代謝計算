<!DOCTYPE html>
<html lang="ja">
<head>
  <meta charset="UTF-8" />
  <title>基礎代謝計算アプリ</title>
</head>
<body>
  <h1>基礎代謝計算（BMR）</h1>
  <form id="bmrForm">
    <label>年齢: <input type="number" id="age" required></label><br>
    <label>性別: 
      <select id="gender">
        <option value="male">男性</option>
        <option value="female">女性</option>
      </select>
    </label><br>
    <label>身長(cm): <input type="number" id="height" required></label><br>
    <label>体重(kg): <input type="number" id="weight" required></label><br>
    <button type="submit">計算する</button>
  </form>
  <p id="result"></p>

  <script>
    document.getElementById('bmrForm').addEventListener('submit', function(e) {
      e.preventDefault();
      const age = parseInt(document.getElementById('age').value);
      const height = parseFloat(document.getElementById('height').value);
      const weight = parseFloat(document.getElementById('weight').value);
      const gender = document.getElementById('gender').value;

      let bmr = 0;
      if (gender === "male") {
        bmr = 10 * weight + 6.25 * height - 5 * age + 5;
      } else {
        bmr = 10 * weight + 6.25 * height - 5 * age - 161;
      }

      document.getElementById('result').textContent = `あなたの基礎代謝は約 ${Math.round(bmr)} kcal/日です。`;
    });
  </script>
</body>
</html>
