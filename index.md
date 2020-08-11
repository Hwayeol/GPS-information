## Welcome to GitHub Pages

You can use the [editor on GitHub](https://github.com/Hwayeol/GPS-information/edit/gh-pages/index.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
<!DOCTYPE html>
<html>

<head>
  <meta charset="UTF-8">
  <title>Insert title here</title>
  <link rel="stylesheet" href="http://code.jquery.com/mobile/1.4.5/jquery.mobile-1.4.5.min.css"/>
  <script src="https://threejs.org/build/three.min.js"></script>
  <script src="http://code.jquery.com/jquery-1.11.1.min.js"></script>
  <script src="http://code.jquery.com/mobile/1.4.5/jquery.mobile-1.4.5.min.js"></script>
  <script>
    $(function() {
        // Geolocation API에 액세스할 수 있는지를 확인
        if (navigator.geolocation) {
            //위치 정보를 정기적으로 얻기
            var id = navigator.geolocation.watchPosition(
                    function(pos) {
                        $('#latitude').html(pos.coords.latitude);     // 위도
                        $('#longitude').html(pos.coords.longitude); // 경도
                    });

            // 버튼 클릭으로 감시를 중지
            $('#btnStop').click(function() {
                navigator.geolocation.clearWatch(id);
            });
        } else {
            alert("이 브라우저에서는 Geolocation이 지원되지 않습니다.")
        }

    });
</script>
</head>
<body>
    <ul>
        <li>위도:<span id="latitude"></span></li>
        <li>경도:<span id="longitude"></span></li>
    </ul>
    <input id="btnStop" type="button" value="감시를 끝낸다" />
</body>
</html>
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/Hwayeol/GPS-information/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
