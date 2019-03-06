---
layout: post
title:  "Tìm hiểu ASP.NET SignalR"
author: blackeye
categories: [ .net, identity, tim-hieu]
image: assets/images/8.jpg
dotnet: true
---

## 1. SignalR là gì ?
ASP.NET SignalR là một thư viện cho các lập trình viên Asp.Net đơn giản hóa quá trình thêm chức năng web real-time trong phát triển ứng dụng. Real-time web functionality là gì ? Đó là khả năng server đẩy những nội dung tới client đã được kết nối một cách tức thì. Nó khác với giao thức HTTP thông thường: server đợi những yêu cầu từ client và trả về nội dung tương ứng.

SignalR có thể sử dụng trong bất kì chức năng web real-time nào. Trong đó ứng dụng chat trên web là một ví dụ điển hình. Ngoài ra, các ứng dụng cho dashboards, monitoring, collaborative là những gợi ý cho việc sử dựng SignalR.

SignalR cung cấp một API đơn giản cho việc tạo server-to-client remote procedure call (RPC) để gọi những hàm javascript trong trình duyệt (và những nền tảng khác) từ code .Net của server-side. SignalR cũng bao gồm API cho việc quản lý kết nối (connect và disconnect events) và những kết nối nhóm.

![]({{site.baseurl}}/assets/images/dotnetcore/signalr.png)

SignalR xử lý quản lý kết nối một cách tự động, và cho bạn truyền đi thông điệp tới tất cả client đã được kết nối một cách đồng loạt, giống như một chat room. Bạn cũng có thể gửi những thông điệp tới những client được xác định. Kết nối giữa client và server là liên tục, không giống như kết nối HTTP cổ điển, cái mà sẽ thành lập lại kết nối cho mỗi lần giao tiếp.

SignalR là mã nguồn mở, có thể truy cập thông qua [GitHub](https://github.com/signalr)

## 2. SignalR và WebSocket
SignalR sử dụng phương thức truyền tải WebSocket mới, và trở lại với phương thức truyền tải cũ hơn nơi cần thiết. Trong khi bạn có thể đảm bảo viết ứng dụng của bạn sử dụng WebSocket một cách trực tiếp, sử dụng SignalR nghĩa là rất nhiều chức năng mở rộng mà bạn sẽ cần để triển khai, đã được làm sẵn cho bạn. Hầu hết các phần quan trọng, điều này muốn nói rằng bạn có thể code ứng dụng của bạn với những ưu điểm của WebSocket mà không phải lo lắng về việc phân chia code cho những client cũ hơn. SignalR cũng sẽ giúp bạn về những cập nhật của WebSocket, từ đó SignalR sẽ tiếp tục được cập nhật để hỗ trợ nhữn thay đổi trong truyền tải tầng bên dưới, cung cấp cho ứng dụng của bạn một giao diện thống nhất xuyên suốt các phiên bản của WebSocket.

Trong khi bạn đã có thể chắc chắn tạo một giải pháp sử dụng WebSocket, SignalR cung cấp tất cả chức năng bạn sẽ cần để viết theo cách bạn muốn, giống như việc trở lại các phương thức truyền tải khác và xem xét lại ứng dụng của bạn cho những cập nhật tới WebSocket.

## 3. Transports và fallbacks
SignalR là một tầng trừu tượng trên một số truyền tải mà yêu cầu để làm công việc thời gian thực giữa client và server. Một kết nối SignalR bắt đầu nư một HTTP, và tiếp theo được đẩy lên một kết nối WebSocket nếu nó là có sẵn. WebSocket là một ý tưởng truyền tải cho SignalR, vì nó làm cho việc sử dựng bộ nhớ server hiệu quả nhất, có độ trễ thấp nhất, và có những tính năng cơ bản nhất (như giao tiếp hai chiều đầy đủ giữa client và server), nhưng nó cũng có những yêu cầu nghiêm ngặt nhất: WebSocket yêu cầu server sử dụng Windows Server 2012 hoặc Windows 8, và .Net 4.5. Nếu những yêu cầu này không được đáp ứng, SignalR sẽ cố gắng để sử dụng những truyền tải khác để làm những kết nối của nó.

## 4. HTML 5 transports
Những truyền tải này phụ thuộc trên việc hỗ trợ HTML 5. Nếu trình duyệt client không hỗ trợ chuẩn HTML 5, truyền tải cũ sẽ được sử dụng.
* **WebSocket** (nếu cả server và client cho biết chúng có thể hỗ trợ WebSocket). WebSocket là truyền tải duy nhất để tạo sự liên tục thực sự, kết nối hai chiều giữa client và server. Tuy nhiên, WebSocket cũng có những yêu cầu nghiêm ngặt nhất; nó cũng chỉ được hỗ trợ đầy đủ trong phiên bản mới nhất của IE, Google Chrome và Mozilla Firefox và chỉ một phần của các trình duyệt khác như Opera và Safari.
* **Server Sent Event**, cũng được biết như EventSource (nếu trình duyệt hỗ trợ Server Sent Events, nó là thành phần cơ bản của tất cả trình duyệt ngoại trừ IE).
## 5. Comet transports
Những truyền tải tầng bên dưới được dựa trên chế độ ứng dụn web Comet, trong đó một trình duyệt hoặc client khác duy trì long-held HTTP request, mà server có thể sử dụng để đẩy dữ liệu tới client mà không cần client yêu cầu cụ thể nào.
* **Forever Frame** (chỉ dành cho IE). Forever frame tạo một IFrame ấn cái mà tạo yêu cầu tới một đích cuối trên server mà không hoàn chỉnh. Tiếp theo Server gửi script một cách liên tục tới client để thực thi trực tiếp, cung cấp một kết nối thời gian thực một chiều từ server tới client. Kết nối từ client tới server sử dụng phân chia kết nối từ server tới kết nối client, 

## 8. Specifying a transport
Thỏa thuận một phương thức truyền tải sẽ mất một chi phí nhất định về thời gian và tài nguyên client/server. Nếu khả năng của client đã được biết thì một truyền tải có thể chỉ định khi kết nối client bắt đầu. Đoạn code dưới đây trình bày việc bắt đầu một kết nối sử dụng truyền tải Ajax Long Polling. Nếu được biết client không hỗ trợ bất kì giao thức nào khác:

    connection.start({transport: 'longPolling'});

Bạn có thể chỉ định một thứ tự gọi nếu bạn muốn client cố gắng chỉ định những giao thức truyền tải

**(continue)**

## 9. Connection và Hubs
SignalR API chứa hai chế độ cho việc giao tiếp giữa client và server: Persistent Connection và Hubs.

Một kết nối đại diện một endpoint đơn giản cho việc gửi single-recipient, grouped hoặc broadcast messages. Persistent Connection API (được biểu diễn trong .NET core bởi PersistentConnection class) đưa lập trình viên truy cập trực tiếp với low-level của giao thức giao tiếp mà SignalR trình bày ra. Việc sử dụng chế độ giao tiếp kết nối sẽ là quen thuộc với những lập trình viên mà đã sử dụng connection-based APIs giống như WCF.

Một Hub làm một high-level đã xây dựng trên Connection API mà cho phép client và server gọi những methods của nhau một cách trực tiếp. SignalR xử lý việc điều phối qua biên giới máy như ảo thuật, cho phép clients gọi các methods trên server một cách dễ dàng như các methods cục bộ và ngược lại. Việc sử dụng chế độ giao tiếp Hubs sẽ là quen thuộc với lập trình viên mà đã sử dụng APIs triệu gọi từ xa giống như .Net Remoting. Sử dụng Hub cũng cho phép bạn truyền "strongly typed parameters" tới methods, enabling model binding.

## 10. Architecture diagram - Biểu đồ kiến trúc
Biểu đồ bên dưới trình bày mối quan hệ giữa Hubs, Persistent Connections và các công nghệ bên dưới được sử dụng cho nhưng giao thức truyền tải.

![]({{site.baseurl}}/assets/images/dotnetcore/signalr-.png)

## 11. Hubs làm việc như thế nào ?
Khi code bên server gọi một method trên client, một gói được gửi qua truyền tải chủ động cái mà chứa tên và những tham số của method được gọi (khi một đối tượng được gửi đi như một tham số của method, nó được serialized sử dụng JSON). Tiếp theo Client khớp tên method với những medthods được định nghĩa bên code client. Nếu có một trùng khớp, client method sẽ thực thi việc sử dụng deserialized parameter data.

Việc gọi method có thể được giám sát bởi sử dụng các công cụ như Fiddler. Hình ảnh dưới đây trình bày một method call gửi từ một SignalR server tới một trình duyệt client trong Logs pane của Fiddler. Method call đã được gửi từ Hub được gọi là MoveeShapeHib và method được gọi là updateShape.

![]()

## 12. Chọn một chế độ giao tiếp
Hầu hết các ứng dụng nên dùng Hubs API. Connection API có thể được sử dụng trong các trường hợp sau đây:
* Định dạng của thông điệp thực sự gửi cần được chỉ định.
* Lập trình viên thích làm việc với mô hình messaging và dispatching hơn là mô hình truy cập từ xa.
* Ứng dụng hiện cómà sử dụng mô hình messaging đang được chuyển qua sử dụng SignalR.

Trên đây là những khái niệm, giao thức, mô hình của SignalR. Bạn có thể tham khảo bài viết gốc bằng tiếng Anh theo link: [http://www.asp.net/signalr/overview/getting-started/introduction-to-signalr](http://www.asp.net/signalr/overview/getting-started/introduction-to-signalr)