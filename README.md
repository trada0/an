<!DOCTYPE html>
<html lang="vi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Chuyển hướng theo giờ</title>
    <!-- Thêm meta để ngăn trình duyệt lưu cache trang web cũ -->
    <meta http-equiv="Cache-Control" content="no-cache, no-store, must-revalidate" />
    <meta http-equiv="Pragma" content="no-cache" />
    <meta http-equiv="Expires" content="0" />
    <style>
        body {
            font-family: Arial, sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
            background-color: #f4f4f9;
        }
        .loader {
            text-align: center;
        }
        .loader h2 {
            color: #333;
        }
        .loader p {
            color: #888;
        }
    </style>
</head>
<body>

    <div class="loader">
        <h2>Đang kiểm tra thời gian...</h2>
        <p>Hệ thống sẽ tự động chuyển hướng bạn trong vài giây.</p>
    </div>

    <script>
        // Lấy giờ hiện tại của thiết bị (tính theo múi giờ địa phương)
        const now = new Date();
        const hour = now.getHours();
        
        let targetUrl = "";

        // Điều kiện 1: Từ 8h00 đến 17h59 (18h) -> Chuyển sang truyen123
        if (hour >= 8 && hour < 18) {
            targetUrl = "https://truyen123.com/teetmm";
        } 
        // Điều kiện 2: Từ 18h01 đến 7h59 -> Chuyển sang Shopee
        // Logic: Giờ >= 18 hoặc Giờ < 8
        else {
            targetUrl = "https://s.shopee.vn/6ff84cCH35";
        }

        // Thực hiện chuyển hướng (Redirect)
        if (targetUrl !== "") {
            window.location.href = targetUrl;
        }
    </script>
</body>
</html>