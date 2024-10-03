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
    <div class="carousel-indicators">
        <button type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide-to="0" class="active" aria-current="true" aria-label="Slide 1"></button>
        <button type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide-to="1" aria-label="Slide 2"></button>
        <button type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide-to="2" aria-label="Slide 3"></button>
    </div>
    <div class="carousel-inner">
        <div class="carousel-item active">
            <img src="https://search.pstatic.net/sunny/?src=https%3A%2F%2Fmedia.licdn.com%2Fdms%2Fimage%2FC5612AQFB2wgvyvJgtw%2Farticle-cover_image-shrink_720_1280%2F0%2F1638590650925%3Fe%3D2147483647%26v%3Dbeta%26t%3DsGdKRw4Xez-OPFXEHKqQsPTNSk6VVczcwnb-1-Tc2Gs&type=sc960_832" class="d-block w-100" alt="First slide">
            <div class="overlay">Network Slicing</div>
        </div>
        <div class="carousel-item">
            <img src="https://search.pstatic.net/sunny/?src=https%3A%2F%2Fmedia-exp1.licdn.com%2Fdms%2Fimage%2FD4E12AQHKEg8wMQqB2Q%2Farticle-cover_image-shrink_720_1280%2F0%2F1666023444578%3Fe%3D2147483647%26v%3Dbeta%26t%3DLtqVVBH-S9_dVCjNkE5pCUECshvI77AjKL4ygiyLASA&type=sc960_832" class="d-block w-100" alt="Second slide">
            <div class="overlay">Mobile network</div>
        </div>
        <div class="carousel-item">
            <img src="https://search.pstatic.net/common/?src=http%3A%2F%2Fblogfiles.naver.net%2F20091013_61%2Fkaiser38_1255412195831oOtX5_jpg%2Fa_kaiser38.jpg&type=sc960_832" class="d-block w-100" alt="Third slide">
            <div class="overlay">LDPC</div>
        </div>
    </div>
    <button class="carousel-control-prev" type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide="prev">
        <span class="carousel-control-prev-icon" aria-hidden="true"></span>
        <span class="visually-hidden">Previous</span>
    </button>
    <button class="carousel-control-next" type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide="next">
        <span class="carousel-control-next-icon" aria-hidden="true"></span>
        <span class="visually-hidden">Next</span>
    </button>
</div>

<!-- Bootstrap JS -->
<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha1/dist/js/bootstrap.bundle.min.js"></script>

</body>
</html>
