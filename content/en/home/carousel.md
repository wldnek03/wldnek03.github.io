<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My Hugo Site</title>

<!-- Bootstrap CSS -->
<link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha1/dist/css/bootstrap.min.css" rel="stylesheet">
    <style>
        .carousel-control-prev-icon,
        .carousel-control-next-icon {
            background-color: black; 
        }
        .carousel-item {
            position: relative;
        }
        .overlay {
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background-color: rgba(0, 0, 0, 0.5); /* 검은색 반투명 레이어 */
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 1.5rem; /* 텍스트 크기 조정 */
            text-align: center;
        }
    </style>    
</head>
<body>
<!-- 이미지 슬라이더 추가 -->
<div id="carouselExampleIndicators" class="carousel slide" data-bs-ride="carousel">
    <div class="carousel-inner">
    </div>
</div>

<!-- Bootstrap JS -->
<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha1/dist/js/bootstrap.bundle.min.js"></script>
</body>
</html>
