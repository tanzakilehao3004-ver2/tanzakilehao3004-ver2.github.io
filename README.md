<!DOCTYPE html>
<html lang="en">
<head>
    <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/css/bootstrap.min.css" integrity="sha384-BVYiiSIFeK1dGmJRAkycuHAHRg32OmUcww7on3RYdg4Va+PmSTsz/K68vbdEjh4u" crossorigin="anonymous">
    <script src="https://ajax.googleapis.com/ajax/libs/angularjs/1.6.4/angular.min.js"></script>
    <meta charset="UTF-8">
    <title>LÀM LẠI website BUỔI 5</title>
</head>
<body>
<div ng-app="MyApp" ng-controller="MyCtrl">
    <nav class="navbar navbar-inverse">
        <div class="container-fluid">
            <div class="navbar-header">
                <a class="navbar-brand" href="#">WebSiteName</a>
            </div>
            <ul class="nav navbar-nav">
                <li class="active"><a href="#">Home</a></li>
                <li><a href="#">Page 1</a></li>
                <li><a href="#">Page 2</a></li>
            </ul>
            <form class="navbar-form navbar-left">
                <div class="form-group">
                    <input type="text" class="form-control" placeholder="Search" ng-model="tu_khoa">
                </div>
                <button type="submit" class="btn btn-default">Submit</button>
            </form>
        </div>
    </nav>
    <div class="container">
        <div class="row">
            <div ng-repeat="video in videos|filter:{title: tu_khoa}" class="col-sm-3">
               <a href="https://www.youtube.com/watch?v={{video.id}}" >
                   <img src="https://i.ytimg.com/vi/{{video.id}}/hqdefault.jpg" alt=" " class="img-thumbnail">
               <div style="overflow: hidden; text-overflow: ellipsis">
                   <span style="white-space: nowrap">
                       {{video.title}}
                   </span>
               </div>

               </a>

            </div>

        </div>
    </div>

</div>
<script>
    var app=angular.module("MyApp", []);
    app.controller("MyCtrl", function ($scope) {
        $scope.videos = [{
            "id": "z1zWvtRucn0", "title": "Tại sao chúng ta cần mua máy ảnh?"
        },
            {"id": "PwrA7yFo7eQ", "title": "Tìm hiểu về Khẩu Độyhfdhfhhfhfbffjf"},
            {"id": "Tdz_4PZtqkE", "title": "Tìm hiểu về Tốc độ chụpfvffddddddddddddddddddđ"},
            {"id": "2-vykRIVdyM", "title": "Tìm hiểu về Độ nhạy sáng IddddddddddddđhbfbhfhhuO"},
            {"id": "e8X6CFfJhH0", "title": "Canon Mahbfhùhfbhfhbfbhrathon"},
            {"id": "N7mh7XWQ3VA", "title": "Anh Không Sao Đâufsfffffèefwefffw- Chi Dân"},
            {"id": "RXMnDgUUl94", "title": "Kiểm tra một tiết về kiểm soát ánh gggggggrsáng!"},
            {"id": "pUfJlmjjfb4", "title": "Chế độ đogggggggggggggggggggggggggggggggggggg sáng"},
            {"id": "2bcNTVqdN6k", "title": "Chế độ lgggggggggggggggggggggấy nét"},
            {"id": "0Heexa11c7k", "title": "Cân Bằng Trắng - White Balance"},
            {"id": "6wQblkWUNKM", "title": "FPT Polytechnic"},
            {"id": "J_0EjKl5kpM", "title": "Blue-BB"}];
    })
</script>
</body>
</html>
