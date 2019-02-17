---
layout: post
title:  "Learn About Jekyll Series - Part01"
author: blackeye
categories: [ jekyll, series, learn, static website ]
image: assets/images/10.jpg
---

# Overview About Jekyll
## What is Jekyll ? - Jekyll là gì ?
Jekyll là trình tạo trang website tĩnh cung cấp một số lợi ích của Hệ thống quản lý nội dung (CMS) trong khi tránh các vấn đề về hiệu suất và bảo mật được giới thiệu bởi các trang web dựa trên cơ sở dữ liệu đó. Đó là "blog" với các tính năng đặc biệt để xử lý nội dung được sắp xếp theo ngày.

Jekyll rất phù hợp với những người cần làm việc ngoại tuyến, người thích sử dụng trình chỉnh sửa nhẹ thay vì biểu mẫu web để duy trì nội dung và muốn sử dụng kiểm soát phiên bản để theo dõi các thay đổi đối với trang web của họ.

## Jekyll Homepage - Tìm hiêu các thành phần trang chủ của Jekyll Website
Sau khi cài đặt 1 trang web jekyll ban đầu. Chạy trên localhost ta được giao diện trang chủ với các thành phần lắp ghép đã được chú thích trong hình dưới:

![]({{site.baseurl}}/Assets/images/jekyll/jekyll-homepage.png)

## Cài đặt cấu hình _config.yml
Phần lớn sức mạnh của Jekyll đến từ khả năng thiết lập thông tin sẽ được lặp lại ở nhiều nơi trên trang web tĩnh trong một tệp nguồn duy nhất, > `_config.yml`

Mặc định > `_config.yml` tạo bởi dòng lệnh > jekyll new  , hoặc tạo và code thủ công với 5 cài đặt hiển thị trên trang chủ:

    title: Your awesome title
    email: your-email@example.com
    description: >- # this means to ignore newlines until "baseurl:"
        Write an awesome description for your new site here. You can edit this
        line in _config.yml. It will appear in your document head meta (for
        Google search results) and in your feed.xml site description.
    baseurl: "" # the subpath of your site, e.g. /blog
    url: "" # the base hostname & protocol for your site, e.g. http://example.com
    twitter_username: jekyllrb
    github_username:  jekyll

    tiêu đề web: tiêu đề tuyệt vời của bạn
    email: email-cua-ban@example.com
    mô tả: >- # điều này nghĩa là bỏ qua các dòng mới cho đến khi "baseurl:"
        Viết một mô tả tuyệt vời cho trang web mới của bạn ở đây. Bạn có thể chỉnh sửa cái này
        dòng trong > _config.yml  . Nó sẽ xuất hiện trong meta đầu tài liệu của bạn (cho
        Kết quả tìm kiếm của Google) và trong mô tả trang web feed.xml của bạn.
    baseurl: "" # đường dẫn phụ của trang web của bạn, ví dụ: /Blog
    url: "" # tên máy chủ và giao thức cơ sở cho trang web của bạn, ví dụ: http://example.com
    twitter_username: username twitter của bạn
    github_username: username github của bạn

    ![]({{site.baseurl}}/Assets/images/jekyll/jekyll-config01.png)

Thông tin này được tự động đưa vào tất cả các trang và bài đăng khác mà chúng ta tạo. Khi chúng ta cần cập nhật một trong những cài đặt này, chúng ta có thể thay đổi tệp này và nó sẽ được cập nhật ở mọi nơi. Để xem điều này trong thực tế, chúng ta sẽ thay đổi các giá trị này.

Chúng ta sẽ thay đổi phần thiết lập với các giá trị dưới đây:

    title: Sammy's Blog
    email: sammy@digitalocean.com
    description: >
    Welcome to my blog!
    github_username: DigitalOcean
    twitter_username: DigitalOcean

Chúng tôi sẽ để url và basurl một mình trong khi chúng tôi đang phát triển và thực hiện bất kỳ điều chỉnh nào khi thời gian triển khai trang web của chúng tôi.

    ![]({{site.baseurl}}/Assets/images/jekyll/config-changes.png)

Có nhiều tùy chỉnh hơn có thể được thực hiện trong _config.yml tệp, nhưng bây giờ chúng tôi sẽ chuyển sang tệp nguồn tiếp theo và lưu ý cách các thay đổi mà chúng tôi đã thực hiện được hiển thị trên phần còn lại của trang web.

## Trang: about.md
Theo About ở góc trên bên phải. Những thay đổi chúng tôi đã thực hiện trong tệp cấu hình được hiển thị ở đây, phía trên và bên dưới nội dung chính của trang Giới thiệu.

Screenshot with the about.md content highlighted

Nội dung trung tâm đó và văn bản liên kết trong tiêu đề, được lưu trữ trong about.md tệp chứa bốn loại nội dung:

### 1. Jekyll Front Matter
Khối ở trên cùng của about.md tập tin bắt đầu và kết thúc với ba dấu gạch ngang là Mặt trận của Jekyll. Nó phải là điều đầu tiên trong tệp, và khi nó hiện diện, nó báo hiệu cho Jekyll rằng tệp cần được phân tích cú pháp. Nó thường bao gồm YAML hợp lệ giữa các dòng để tận dụng các biến được xác định trước, nhưng nó cũng có thể để trống. Một khối Front Matter trống đôi khi hữu ích cho một tệp CSS hoặc một nơi khác mà bạn không cần đặt bất kỳ giá trị nào nhưng bạn muốn truy cập vào các biến.

Trang "Giới thiệu" đặt ba giá trị trong Mặt trận của nó:

   ---
   layout: page
   title: About
   permalink: /about/
   ---
Bố trí:
Bố cục loại bỏ nội dung lặp lại như tiêu đề, chân trang và menu để làm cho trang web dễ bảo trì hơn. Jekyll đi kèm với ba bố cục: default, pagevà post. Mỗi người đều có những đặc điểm riêng. Trong trường hợp này, một liên kết menu đến giá trị tiêu đề, â € œAboutâ € xuất hiện trong điều hướng tiêu đề vì bố cục được đặt thành â € œpage.â €

Chức vụ:
Ngoài việc được sử dụng làm văn bản liên kết trong điều hướng tiêu đề, tiêu đề cũng được sử dụng làm tiêu đề trang hiển thị, được định dạng bằng thẻ Tiêu đề 1 và dưới dạng trang <title>, là văn bản xuất hiện trên thanh trình duyệt và khi trang được đánh dấu trang.

Liên kết:
Jekyll tự động tạo các thư mục và tệp HTML từ các tệp nguồn này xác định URL của trang. Permalink cho phép bạn ghi đè lên hành vi mặc định. Ở đây nó làm cho URL trang được http://203.0.113.0:4000/about/ thay vì http://203.0.113.0 :4000/about.html.

### 2. Văn bản hiển thị
Nội dung trang bắt đầu sau Mặt trận. Văn bản ở đây xuất hiện trên trang, chẳng hạn như â € œĐây là cơ sở Jekyll 3. theme.â €

### 3. Markdown
Đánh dấu là một phần của nội dung trang chính và kiểm soát định dạng nội dung. Nó sẽ được phân tích thành HTML cho trang tĩnh. Đánh dấu thường được các nhà văn nội dung ưa thích hơn HTML vì nó được thiết kế để dễ đọc và dễ viết hơn.

### 4. Chỉ thị mẫu chất lỏng
Jekyll sử dụng Liquid làm công cụ tạo mẫu để bao gồm các yếu tố động. Các chỉ thị Liquid xuất hiện giữa các dấu ngoặc nhọn như {% include icon-github.html username="jekyll" %}.

Hãy thực hiện một số thay đổi cho trang này để xem trang web bị ảnh hưởng như thế nào.

Thay đổi tiêu đề
Chúng tôi sẽ thực hiện một thay đổi nhỏ và gọi trang "Giới thiệu về tôi" thay vì chỉ "Giới thiệu":


 
nano ~/www/about.md
~/www/about.md

---
. . .
title: "About me"
. . .
---
Khi bạn hoàn tất, lưu và thoát tệp.

Thay đổi sẽ xuất hiện ở ba vị trí và liên kết menu sẽ được cập nhật trên tất cả các trang của trang:
Screenshot with the about.md with title changes highlighted

Thêm trang mới
Tiếp theo, chúng tôi sẽ thêm một trang "Liên hệ" vào trang web và sử dụng một chút đánh dấu để bao gồm một hình ảnh.

Chúng ta sẽ bắt đầu bằng cách làm assets thư mục để giữ hình ảnh của chúng tôi:

mkdir ~/www/assets
Sau đó, chúng tôi sẽ chuyển hình ảnh đến máy của chúng tôi bằng wget. Các -O cờ sẽ chuyển nó đến thư mục chúng ta đã tạo. Cờ yêu cầu chúng tôi cũng chỉ định tên tệp, vì vậy chúng tôi sẽ:

wget -O ~/www/assets/postcard.jpg http://assets.digitalocean.com/articles/jekyll-1604/postcard.jpg
Khi hình ảnh được đặt cục bộ, chúng tôi sẽ tạo trang mới:

nano ~/www/contact.md
~/www/contact.md

---
layout: page
title: "Send me a postcard!"
---

DigitalOcean\\
Attn: Sammy Shark\\
101 Avenue of the Americas\\
New York, NY 10013

![A postcard](/assets/postcard.jpg)
Chúng ta hãy xem xét kỹ hơn markdown. Đầu tiên, dấu gạch chéo kép, \\, ở cuối mỗi dòng sẽ trả về mà không cần thêm khoảng trắng. Thứ hai, hình ảnh được hiển thị với nhãn hiệu này ![](). Dấu chấm than báo hiệu rằng liên kết sau đây là một hình ảnh. Các dấu ngoặc chứa văn bản thay thế sẽ được sử dụng nếu hình ảnh không được tải hoặc khách truy cập đang sử dụng trình đọc màn hình. Các dấu ngoặc đơn chứa liên kết đến tệp hình ảnh. Bạn có thể tìm hiểu thêm về phong cách đánh dấu mặc định của Jekyll trên trang web kramdown.

Lưu và thoát tệp, sau đó tải lại trang. Liên kết mới sẽ xuất hiện, được sắp xếp theo thứ tự bảng chữ cái dựa trên tên của tệp.

Với các tệp mới tại chỗ, phần đầu của cấu trúc tệp của chúng tôi bây giờ trông giống như sau:

âââ about.md
âââ assets
â   âââ postcard.jpg
âââ _config.yml
âââ contact.md
Trang web thực sự trông giống như sau:

Screenshot of the new Contact page

Nhấp vào tiêu đề trang web để quay lại trang chủ, nơi bạn sẽ tìm thấy liên kết mới được bao gồm trong điều hướng tiêu đề.

Chú thích: Thông thường có biểu mẫu web tương tác trên trang Liên hệ. Jekyll không cung cấp bất kỳ xử lý biểu mẫu được tích hợp nào, nhưng bạn có thể sử dụng các dịch vụ dựa trên đám mây như Disqus, Formspree hoặc FormKeep hoặc lưu trữ các dịch vụ của riêng bạn.

Bài đăng: _posts /YYYY-MM-DD-welcome-to-jekyll.markdown
Theo liên kết "Chào mừng bạn đến với Jekyll" để xem bài đăng blog mẫu được cung cấp.

Screenshot of the Welcome to Jekyll post with the main content area highlighted

Các _posts thư mục chứa các tệp được đặt tên đặc biệt, theo định dạng YYYY-MM-DD-Words-in-Title. Nếu bài đăng của bạn không được đặt tên theo định dạng này, bài đăng đó sẽ không được phân tích cú pháp. Nếu tên tệp có ngày được đặt trong tương lai, trang sẽ không được phân tích cú pháp cho trang web tĩnh. Đặt tên tệp với một ngày trong tương lai làm cho phép lược đồ đặt tên được sử dụng kết hợp với cron hoặc các chiến lược tự động hóa khác để xuất bản bài đăng sau ngày và giờ cụ thể. Các tệp bài đăng có thể kết thúc bằng .markdown, .md, .htmlhoặc các tiện ích khác khi tùy chỉnh chuyển đổi đã được cài đặt.

Bài viết bắt đầu với Front Matter. Front Matter là bắt buộc đối với mỗi tệp bài đăng vì nó chứa các giá trị như ngày quan trọng đối với việc tạo trang web.

~/www/_posts/2016-08-31-welcome-to-jekyll.markdown

---
layout: post
title:  "Welcome to Jekyll!"
date:   2016-08-31 17:35:19 +0000
categories: jekyll update
---
Bố trí:
Mặc dù có thể bố cục khá khác nhau, bố cục cho bài đăng rất giống với mặc định. Có các biến thể trong HTML <head> ... </head> trong đó nội dung trang khác nhau và nội dung giữa <div class="wrapper"> ... </div> thẻ, nhưng phần còn lại là giống nhau. Sự khác biệt có thể nhìn thấy duy nhất trên chính trang đó là sự bao gồm tự động của giá trị ngày tháng của Mặt trận bên dưới tiêu đề.

Chức vụ:
Tiêu đề xuất hiện cả hai như Tiêu đề 1 trên chính bài đăng trên blog và làm Tiêu đề 2 trên trang chỉ mục.

Ngày:
Ngày, được đặt ở đây, sẽ xác định ngày được hiển thị trên cả trang chủ và bài đăng. Đó là ngày này cũng sẽ xác định URL của bài đăng mà chúng tôi sẽ sớm tìm hiểu chi tiết hơn.

Chú thích: Ngày trong Front Matter không có mối quan hệ trực tiếp với ngày bắt đầu tên tệp. Tên tệp phải bắt đầu bằng một ngày ở định dạng thích hợp để được phân tích cú pháp. Nếu nó được đặt tên theo một ngày trong tương lai, nó sẽ không được phân tích cú pháp cho đến khi quá trình xây dựng trang web tiếp theo sau ngày đó. Trong khi đó, Mặt trận Matter xác định cấu trúc thư mục sau khi tệp Là được phân tích cú pháp và được sử dụng làm giá trị được hiển thị trên trang chủ và bài đăng.

Thể loại: Danh mục dành riêng cho bài đăng và được sử dụng để nhóm nội dung theo chủ đề. Theo mặc định, chúng không hiển thị trên trang, mặc dù chúng có thể được thêm vào mẫu tùy chỉnh.
Các tệp còn lại
Chúng tôi đã xem xét chặt chẽ ba tệp cho đến nay, _config.yml, about.mdvà _posts/YYYY-MM-DD-welcome-to-jekyll.markdown. Dưới đây là tổng quan ngắn gọn về các tệp ít hiển thị trực tiếp từ trình duyệt:

### main.scss:
Jekyll sử dụng Syntactically Awesome Style Sheets (Sass), mà nó biên dịch thành CSS thông thường mỗi khi trang web được xây dựng lại. Các tệp .sass nằm trong css danh mục.

### feed.xml:
Jekyll cung cấp một nguồn cấp dữ liệu RSS, cũng được xây dựng mỗi khi trang web tĩnh được xây dựng lại, cho phép các trang web tổng hợp các bài đăng và cung cấp cách để người dùng đăng ký.

### Gemfile và Gemfile.lock:
Gemfile liệt kê các plugin cho Jekyll được cài đặt với bundle chỉ huy. Khi chúng được cài đặt, tệp Gemfile.lock được tạo để theo dõi phiên bản cụ thể của các plugin đã được cài đặt.

Trong số bốn tệp này, chỉ CSS ảnh hưởng đến việc trình bày nội dung. Nếu bạn đặc biệt quan tâm đến Jekyll và Sass, bạn có thể tìm hiểu thêm về nó từ Trang web ví dụ của Jekyll về tích hợp Sass.

Phần kết luận
Trong hướng dẫn này, chúng tôi đã khám phá nội dung soạn sẵn mà Jekyll cung cấp khi chúng tôi tạo một trang web mới và thực hiện một vài thay đổi để chứng minh cách các tệp nguồn kết hợp với nhau trên các trang web. Điều này làm cho trang web dễ bảo trì hơn bằng cách đặt giá trị ở một nơi duy nhất, nơi chúng có thể được cập nhật bằng một bản chỉnh sửa thay vì phải thay đổi mọi tệp. Nó cũng cho phép các bài đăng được bao gồm động trên trang chủ, do đó bạn không phải lo lắng về cách cập nhật thủ công một trang khác để làm nổi bật bài đăng mới.

Trong Phần 3, chúng tôi sẽ xem xét cấu trúc tệp của trang web tĩnh, cách cấu trúc đó được phản ánh trong URL của các trang và bài đăng của chúng tôi theo mặc định và cách ghi đè hành vi mặc định.