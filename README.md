<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Introduction to 3 People</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            line-height: 1.6;
            margin: 20px;
            padding: 20px;
            background-size: cover;
            background-position: center;
            background-repeat: no-repeat;
            background-image: url('default-background.jpg'); /* Ảnh nền mặc định */
        }
        .container {
            max-width: 800px;
            margin: 0 auto;
            padding: 20px;
            background-color: rgba(255, 255, 255, 0.8);
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }
        .person {
            margin-bottom: 20px;
        }
        .person h2 {
            color: #333;
        }
        .person .avatar {
            width: 100px;
            height: 100px;
            border-radius: 50%;
            overflow: hidden;
            margin-right: 10px;
            float: left;
        }
        .person .info {
            margin-left: 120px; /* Để tránh lấn lên phần ảnh */
        }
        .background-upload {
            margin-bottom: 10px;
            display: none; /* Ẩn phần chọn file */
        }
        input[type="file"] {
            display: none; /* Ẩn input file mặc định */
        }
        label {
            display: inline-block;
            padding: 10px 15px;
            background-color: #3498db;
            color: white;
            cursor: pointer;
            border-radius: 5px;
        }
        label:hover {
            background-color: #2980b9;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Introduction to 3 People</h1>

        <!-- Đổi ảnh nền -->
        <div class="background-upload">
            <input type="file" id="background-image" accept="image/*" onchange="changeBackground(event)">
            <label for="background-image">Chọn ảnh làm nền</label>
        </div>
        
        <!-- Thông tin người thứ nhất -->
        <div class="person">
            <div class="avatar">
                <img src="avatar.jpg" alt="">
            </div>
            <div class="info">
                <h2>Person 1: Tuấn (Nhóm trưởng)</h2>
                <ul>
                    <li><strong>Tên:</strong> Đinh Quốc Tuấn (Nhóm trưởng)</li>
                    <li><strong>Ngày sinh:</strong> 2004</li>
                    <li><strong>Khóa học:</strong> Công nghệ thông tin</li>
                    <li><strong>Công việc:</strong> Lập kế hoạch cho dự án</li>
                </ul>
            </div>
        </div>

        <!-- Thông tin người thứ hai -->
        <div class="person">
            <div class="avatar">
                <img src="avatar.jpg" alt="">
            </div>
            <div class="info">
                <h2>Person 2: Nhật</h2>
                <ul>
                    <li><strong>Tên:</strong> Phạm Quốc Nhật</li>
                    <li><strong>Ngày sinh:</strong> 2004</li>
                    <li><strong>Khóa học:</strong> Công nghệ thông tin</li>
                    <li><strong>Công việc:</strong> Thiết kế giao diện</li>
                </ul>
            </div>
        </div>

        <!-- Thông tin người thứ ba -->
        <div class="person">
            <div class="avatar">
                <img src="avatar.jpg" alt="">
            </div>
            <div class="info">
                <h2>Person 3: Hoàng</h2>
                <ul>
                    <li><strong>Tên:</strong>Trần Minh Hoàng</li>
                    <li><strong>Ngày sinh:</strong> 2004</li>
                    <li><strong>Khóa học:</strong> Công nghệ thông tin</li>
                    <li><strong>Công việc:</strong> Làm phần github</li>
                </ul>
            </div>
        </div>
    </div>

    <script>
        // Function thay đổi ảnh nền
        function changeBackground(event) {
            var file = event.target.files[0];
            var reader = new FileReader();
            reader.onload = function(e) {
                document.body.style.backgroundImage = 'url(' + e.target.result + ')';
            };
            reader.readAsDataURL(file);
        }
    </script>
</body>
</html>
