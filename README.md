<!DOCTYPE html>
<html lang="fa">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>فروشگاه مهرگان زاگرس</title>
<style>
  body {
    font-family: Tahoma, sans-serif;
    background-color: #f9f9f9;
    margin: 0; padding: 0;
    direction: rtl;
  }
  header {
    background-color: #004080;
    color: white;
    padding: 15px 20px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    flex-wrap: wrap;
  }
  header h1 {
    margin: 0;
  }
  nav a {
    color: white;
    text-decoration: none;
    margin: 0 12px;
    font-weight: bold;
  }
  nav a:hover {
    text-decoration: underline;
  }
  .container {
    max-width: 1100px;
    margin: 20px auto;
    padding: 0 20px;
  }
  /* محصولات */
  .products {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    gap: 20px;
  }
  .product {
    background: white;
    border: 1px solid #ddd;
    border-radius: 8px;
    width: 280px;
    padding: 15px;
    box-shadow: 0 0 10px rgba(0,0,0,0.1);
    text-align: center;
  }
  .product img {
    width: 100%;
    height: 180px;
    object-fit: contain;
    border-radius: 6px;
  }
  .product h3 {
    margin: 15px 0 10px 0;
    color: #004080;
  }
  .product p {
    color: #555;
    font-size: 14px;
    min-height: 40px;
  }
  .price {
    font-weight: bold;
    color: #e60000;
    margin: 10px 0;
    font-size: 18px;
  }
  .buy-btn {
    background-color: #004080;
    color: white;
    border: none;
    padding: 10px 15px;
    border-radius: 5px;
    cursor: pointer;
    font-size: 16px;
    transition: background-color 0.3s ease;
  }
  .buy-btn:hover {
    background-color: #0066cc;
  }
  /* فرم ثبت سفارش */
  form {
    background: white;
    padding: 20px;
    border-radius: 8px;
    box-shadow: 0 0 12px rgba(0,0,0,0.1);
    max-width: 600px;
    margin: 30px auto;
  }
  form h2 {
    color: #004080;
    margin-bottom: 20px;
    text-align: center;
  }
  label {
    display: block;
    margin-top: 15px;
    font-weight: bold;
    color: #333;
  }
  input, select, textarea {
    width: 100%;
    padding: 10px;
    margin-top: 6px;
    border-radius: 5px;
    border: 1px solid #ccc;
    font-size: 14px;
    box-sizing: border-box;
  }
  textarea {
    resize: vertical;
  }
  button.submit-btn {
    background-color: #004080;
    color: white;
    border: none;
    padding: 12px 20px;
    margin-top: 20px;
    border-radius: 6px;
    cursor: pointer;
    font-size: 16px;
    width: 100%;
  }
  button.submit-btn:hover {
    background-color: #0066cc;
  }
  /* صفحه تماس با ما */
  .contact-info {
    background: white;
    max-width: 600px;
    margin: 30px auto;
    padding: 20px;
    border-radius: 8px;
    box-shadow: 0 0 12px rgba(0,0,0,0.1);
    text-align: center;
    font-size: 16px;
    color: #333;
  }
  .contact-info h2 {
    color: #004080;
    margin-bottom: 15px;
  }
  .contact-info p {
    margin: 8px 0;
  }
  /* درباره شرکت */
  .about {
    background: white;
    max-width: 900px;
    margin: 30px auto;
    padding: 25px;
    border-radius: 8px;
    box-shadow: 0 0 12px rgba(0,0,0,0.1);
    color: #333;
    line-height: 1.6;
  }
  .about h2 {
    color: #004080;
    margin-bottom: 15px;
    text-align: center;
  }
  footer {
    background-color: #004080;
    color: white;
    text-align: center;
    padding: 15px 10px;
    margin-top: 40px;
    font-size: 14px;
  }
  /* ریسپانسیو */
  @media(max-width: 700px){
    .products {
      flex-direction: column;
      align-items: center;
    }
    .product {
      width: 90%;
    }
  }
</style>
<script>
  function buyProduct(name) {
    alert(name + " به سبد خرید اضافه شد! متشکریم از خرید شما.");
  }
  function submitOrder(event) {
    event.preventDefault();
    const name = document.getElementById("custName").value.trim();
    const phone = document.getElementById("custPhone").value.trim();
    const product = document.getElementById("productSelect").value;
    const address = document.getElementById("custAddress").value.trim();
    if (!name || !phone || !address) {
      alert("لطفاً همه فیلدها را پر کنید.");
      return;
    }
    alert("سفارش شما ثبت شد!\n\n" +
          "نام: " + name + "\n" +
          "شماره تلفن: " + phone + "\n" +
          "محصول: " + product + "\n" +
          "آدرس: " + address + "\n\n" +
          "با شما تماس گرفته خواهد شد.");
    document.getElementById("orderForm").reset();
  }
</script>
</head>
<body>

<header>
  <h1>فروشگاه مهرگان زاگرس</h1>
  <nav>
    <a href="#products">محصولات</a>
    <a href="#order">ثبت سفارش</a>
    <a href="#contact">تماس با ما</a>
    <a href="#about">درباره ما</a>
  </nav>
</header>

<div class="container">

  <!-- محصولات -->
  <section id="products">
    <h2 style="text-align:center; color:#004080;">محصولات ما</h2>
    <div class="products">
      <div class="product">
        <img src="https://via.placeholder.com/280x180?text=محصول+1" alt="محصول 1" />
        <h3>محصول شماره 1</h3>
        <p>توضیح کوتاه درباره محصول اول شرکت مهرگان زاگرس.</p>
        <div class="price">۴۵۰,۰۰۰ تومان</div>
        <button class="buy-btn" onclick="buyProduct('محصول شماره 1')">خرید</button>
      </div>
      <div class="product">
        <img src="https://via.placeholder.com/280x180?text=محصول+2" alt="محصول 2" />
        <h3>محصول شماره 2</h3>
        <p>توضیح کوتاه درباره محصول دوم شرکت مهرگان زاگرس.</p>
        <div class="price">۶۰۰,۰۰۰ تومان</div>
        <button class="buy-btn" onclick="buyProduct('محصول شماره 2')">خرید</button>
      </div>
      <div class="product">
        <img src="https://via.placeholder.com/280x180?text=محصول+3" alt="محصول 3" />
        <h3>محصول شماره 3</h3>
        <p>توضیح کوتاه درباره محصول سوم شرکت مهرگان زاگرس.</p>
        <div class="price">۷۲۰,۰۰۰ تومان</div>
        <button class="buy-btn" onclick="buyProduct('محصول شماره 3')">خرید</button>
      </div>
    </div>
  </section>

  <!-- فرم ثبت سفارش -->
  <section id="order">
    <form id="orderForm" onsubmit="submitOrder(event)">
      <h2>ثبت سفارش</h2>
      <label for="custName">نام و نام خانوادگی:</label>
      <input type="text" id="custName" name="custName" placeholder="نام خود را وارد کنید" required />
      
      <label for="custPhone">شماره تلفن:</label>
      <input type="tel" id="custPhone" name="custPhone" placeholder="مثلاً 09123456789" pattern="[0-9]{11}" required />
      
      <label for="productSelect">محصول مورد نظر:</label>
      <select id="productSelect" name="productSelect" required>
        <option value="">انتخاب محصول</option>
        <option value="محصول شماره 1">محصول شماره 1</option>
        <option value="محصول شماره 2">محصول شماره 2</option>
        <option value="محصول شماره 3">محصول شماره 3</option>
      </select>
      
      <label for="custAddress">آدرس:</label>
      <textarea id="custAddress" name="custAddress" rows="3" placeholder="آدرس کامل خود را وارد کنید" required></textarea>
      
      <button type="submit" class="submit-btn">ارسال سفارش</button>
    </form>
  </section>

  <!-- تماس با ما -->
  <section id="contact" class="contact-info">
    <h2>تماس با ما</h2>
    <p>شماره تماس: <a href="tel:+982112345678">۰۲۱-۱۲۳۴۵۶۷۸</a></p>
    <p>ایمیل: info@mehrganzagros.com</p>
    <p>آدرس دفتر مرکزی: تهران، خیابان انقلاب، پلاک ۱۲۳</p>
  </section>

  <!-- درباره شرکت -->
  <section id="about" class="about">
    <h2>درباره شرکت مهرگان زاگرس</h2>
    <p>شرکت مهرگان زاگرس از سال ۱۳۹۰ شروع به فعالیت کرده و در زمینه پخش محصولات آرایشی بهداشتی فعالیت می‌کند.  
    این شرکت با ارائه محصولات با کیفیت و خدمات به‌روز، همواره تلاش کرده است رضایت مشتریان خود را جلب کند و تا به امروز به رشد و توسعه مستمر خود ادامه داده است.</p>
    <p>ما به دنبال نوآوری و ارتقاء کیفیت در محصولات خود هستیم تا بتوانیم بهترین‌ها را به شما عرضه کنیم.</p>
  </section>

</div>

<footer>
  <p>© ۲۰۲۵ مهرگان زاگرس. همه حقوق محفوظ است.</p>
</footer>

</body>
</html>
