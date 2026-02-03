
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>موقع بيع البيتزا</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f4;
            margin: 0;
            padding: 0;
            color: #333;
        }
        header {
            background-color: #ff4500;
            color: white;
            text-align: center;
            padding: 20px;
        }
        .container {
            max-width: 800px;
            margin: 20px auto;
            padding: 20px;
            background-color: white;
            border-radius: 8px;
            box-shadow: 0 0 10px rgba(0,0,0,0.1);
        }
        .menu {
            display: flex;
            flex-wrap: wrap;
            justify-content: space-around;
        }
        .pizza-item {
            width: 45%;
            margin: 10px;
            padding: 10px;
            border: 1px solid #ddd;
            border-radius: 5px;
            text-align: center;
        }
        .pizza-item img {
            width: 100%;
            height: 150px;
            object-fit: cover;
            border-radius: 5px;
        }
        .order-form {
            margin-top: 20px;
        }
        input, select, button {
            display: block;
            width: 100%;
            margin: 10px 0;
            padding: 10px;
            border: 1px solid #ccc;
            border-radius: 5px;
        }
        button {
            background-color: #ff4500;
            color: white;
            cursor: pointer;
        }
        button:hover {
            background-color: #e63900;
        }
    </style>
</head>
<body>
    <header>
        <h1>موقع بيع البيتزا الشهير</h1>
        <p>اطلب بيتزا طازجة ومذاقها رائع!</p>
    </header>
    
    <div class="container">
        <h2>قائمة البيتزا</h2>
        <div class="menu">
            <div class="pizza-item">
                <img src="https://via.placeholder.com/300x150?text=بيتزا+مارغريتا" alt="بيتزا مارغريتا">
                <h3>بيتزا مارغريتا</h3>
                <p>جبنة، طماطم، ريحان. السعر: 25 ريال</p>
            </div>
            <div class="pizza-item">
                <img src="https://via.placeholder.com/300x150?text=بيتزا+بيبروني" alt="بيتزا بيبروني">
                <h3>بيتزا بيبروني</h3>
                <p>لحم بيبروني، جبنة. السعر: 30 ريال</p>
            </div>
            <div class="pizza-item">
                <img src="https://via.placeholder.com/300x150?text=بيتزا+خضار" alt="بيتزا خضار">
                <h3>بيتزا خضار</h3>
                <p>فلفل، بصل، زيتون. السعر: 28 ريال</p>
            </div>
            <div class="pizza-item">
                <img src="https://via.placeholder.com/300x150?text=بيتزا+دجاج" alt="بيتزا دجاج">
                <h3>بيتزا دجاج</h3>
                <p>دجاج مشوي، جبنة. السعر: 32 ريال</p>
            </div>
        </div>
        
        <h2>اطلب الآن</h2>
        <form class="order-form" id="orderForm">
            <label for="name">الاسم:</label>
            <input type="text" id="name" required>
            
            <label for="phone">رقم الهاتف:</label>
            <input type="tel" id="phone" required>
            
            <label for="pizza">اختر البيتزا:</label>
            <select id="pizza" required>
                <option value="">-- اختر --</option>
                <option value="مارغريتا">مارغريتا - 25 ريال</option>
                <option value="بيبروني">بيبروني - 30 ريال</option>
                <option value="خضار">خضار - 28 ريال</option>
                <option value="دجاج">دجاج - 32 ريال</option>
            </select>
            
            <label for="quantity">الكمية:</label>
            <input type="number" id="quantity" min="1" required>
            
            <button type="submit">أرسل الطلب</button>
        </form>
    </div>
    
    <script>
        document.getElementById('orderForm').addEventListener('submit', function(event) {
            event.preventDefault();
            const name = document.getElementById('name').value;
            const phone = document.getElementById('phone').value;
            const pizza = document.getElementById('pizza').value;
            const quantity = document.getElementById('quantity').value;
            
            alert(`شكراً ${name}! تم استلام طلبك: ${quantity} ${pizza}. سنتصل بك على ${phone}.`);
            // هنا يمكن إضافة كود لإرسال البيانات إلى خادم حقيقي إذا أردت.
        });
    </script>
</body>
</html>
