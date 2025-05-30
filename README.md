[Tiếng Nhật](/README.md) /
[Tiếng Anh](/docs_i18n/README_en.md) /
[Hàn Quốc](/docs_i18n/README_ko.md)/
[Tiếng Trung](/docs_i18n/README_zh.md)/
[tiếng Đức](/docs_i18n/README_de.md)/
[Tiếng Ả Rập](/docs_i18n/README_ar.md)/
[Hy Lạp](/docs_i18n/README_el.md)/
[Tiếng Tây Ban Nha](/docs_i18n/README_es.md)/
[Tiếng Pháp](/docs_i18n/README_fr.md)/
[Tiếng Ý](/docs_i18n/README_it.md)/
[tiếng Latinh](/docs_i18n/README_la.md)/
[Tiếng Mã Lai](/docs_i18n/README_ms.md)/
[Tiếng Nga](/docs_i18n/README_ru.md)
*Tất cả các ngôn ngữ ngoại trừ tiếng Nhật đều được dịch bằng máy.

##VCClient

VCClient là phần mềm sử dụng AI để thực hiện chuyển đổi giọng nói theo thời gian thực.

##Có gì mới!
* v.2.0.78-beta
* sửa lỗi: Tránh lỗi tải mô hình RVC
* Bây giờ có thể chạy phiên bản 1.x cùng lúc. 
* Số lượng kích thước khối có thể chọn đã được tăng lên.

* v.2.0.77-beta (chỉ dành cho RTX 5090, thử nghiệm)
* Các mô-đun liên quan hiện tương thích với 5090 (hoạt động chưa được xác minh vì nhà phát triển không sở hữu RTX5090)
* v.2.0.76-beta
* Tính năng mới:
* Beatrice: Triển khai hợp nhất loa
* Beatrice: Tự động chuyển cao độ
* Sửa lỗi:
* Đã sửa lỗi khi chọn thiết bị ở chế độ máy chủ
* v.2.0.73-beta
* Tính năng mới:
* Tải xuống mô hình beatrice đã chỉnh sửa
* Sửa lỗi:
* Đã sửa lỗi khiến beatrice v2 pitch và formant không được phản ánh
* Đã sửa lỗi khiến không thể tạo ONNX cho các mô hình sử dụng trình nhúng Applio.

## Tải xuống và liên kết liên quan

Có thể tải xuống phiên bản Windows và M1 Mac từ kho lưu trữ huging face.

* [Kho lưu trữ VCClient](https://huggingface.co/wok000/vcclient000/tree/main)
* [Kho lưu trữ Light VCClient cho Beatrice v2](https://huggingface.co/wok000/light_vcclient_beatrice/tree/main)

*1 Đối với Linux, vui lòng sao chép kho lưu trữ.

### Liên kết liên quan

* [Kho mã đào tạo Beatrice V2](https://huggingface.co/fierce-cats/beatrice-trainer)
* [Mã đào tạo Beatrice V2 phiên bản Colab](https://github.com/w-okada/beatrice-trainer-colab)

### Phần mềm liên quan

* [Trình thay đổi giọng nói thời gian thực VCClient](https://github.com/w-okada/voice-changer)
* [Phần mềm chuyển văn bản thành giọng nói TTSClient](https://github.com/w-okada/ttsclient)
* [Phần mềm nhận dạng giọng nói thời gian thực ASRClient](https://github.com/w-okada/asrclient)

## Tính năng của VC Client

## Hỗ trợ nhiều mô hình AI khác nhau

| Mô hình AI | v.2 | v.1 | Giấy phép |
|---------------------------------------------------------------------------------------------------------- | --------- | -------------------- | ------------------------------------------------------------------------------------------- |
| [RVC ](https://github.com/RVC-Project/Retrieval-based-Voice-Conversion-WebUI/blob/main/docs/jp/README.ja.md) | được hỗ trợ | được hỗ trợ | Xem kho lưu trữ.                                                             |
| [Beatrice v1](https://prj-beatrice.com/) | không có | được hỗ trợ (chỉ thắng) | [Sở hữu](https://github.com/w-okada/voice-changer/tree/master/server/voice_changer/Beatrice) |
| [Beatrice v2](https://prj-beatrice.com/) | được hỗ trợ | không có | [Bản gốc](https://huggingface.co/wok000/vcclient_model/blob/main/beatrice_v2_beta/readme.md) |
| [MMVC](https://github.com/isletennos/MMVC_Trainer) | không có | được hỗ trợ | Xem kho lưu trữ.                                                             |
| [so-vits-svc](https://github.com/svc-develop-team/so-vits-svc) | không có | được hỗ trợ | Xem kho lưu trữ.                                                             |
| [DDSP-SVC](https://github.com/yxlllc/DDSP-SVC) | không có | được hỗ trợ | Xem kho lưu trữ.                                                             |

Hỗ trợ cả cấu hình độc lập và cấu hình mạng

Nó hỗ trợ cả chuyển đổi âm thanh trên máy tính cục bộ và chuyển đổi âm thanh qua mạng.
Bằng cách sử dụng qua mạng, bạn có thể chuyển tải công việc chuyển đổi giọng nói sang thiết bị bên ngoài khi sử dụng đồng thời với các ứng dụng tải cao như trò chơi.

![hình ảnh](https://user-images.githubusercontent.com/48346627/206640768-53f6052d-0a96-403b-a06c-6714a0b7471d.png)

## Hỗ trợ nhiều nền tảng

Windows, Mac(M1), Linux, Google Colab

*1 Đối với Linux, vui lòng sao chép kho lưu trữ.

## Cung cấp REST API

Khách hàng có thể được viết bằng nhiều ngôn ngữ lập trình khác nhau.

Bạn cũng có thể sử dụng trình khách HTTP được tích hợp sẵn trong hệ điều hành, chẳng hạn như curl, để vận hành nó.

## Xử lý sự cố

[Giao tiếp](tutorials/trouble_shoot_communication_ja.md)

## Chữ ký nhà phát triển

Phần mềm này không được nhà phát triển ký tên. Một thông báo cảnh báo sẽ xuất hiện như hình dưới đây, nhưng bạn có thể chạy chương trình bằng cách giữ phím control và nhấp vào biểu tượng. Điều này là do chính sách bảo mật của Apple. Bất kỳ hành động thực hiện nào cũng đều do bạn tự chịu rủi ro.

![hình ảnh](https://user-images.githubusercontent.com/48346627/212567711-c4a8d599-e24c-4fa3-8145-a5df7211f023.png)

## Lời cảm ơn

* [Vật liệu đứng](https://seiga.nicovideo.jp/seiga/im10792934)
* [Irasutoya](https://www.irasutoya.com/)
* [Tsukuyomi-chan](https://tyc.rei-yumesaki.net/)

```
Tính năng tổng hợp giọng nói trong phần mềm này sử dụng dữ liệu giọng nói được cung cấp miễn phí bởi nhân vật miễn phí "Tsukuyomi-chan". 
■ Tsukuyomi-chan Corpus (CV. Yumesaki Rei)
https://tyc.rei-yumesaki.net/material/corpus/
© Rei Yumesaki
```

* [Phòng thu âm giọng nói của Amitaro](https://amitaro.net/)
* [Búp bê bản sao](https://kikyohiroto1227.wixsite.com/kikoto-utau)

## điều khoản dịch vụ

* Về phần mềm thay đổi giọng nói thời gian thực Tsukuyomi-chan, theo các điều khoản sử dụng Tsukuyomi-chan Corpus, việc sử dụng giọng nói đã chuyển đổi cho các mục đích sau là bị nghiêm cấm.

```

■Chỉ trích hoặc tấn công người khác. (Định nghĩa của "phê bình/tấn công" tuân theo giấy phép nhân vật Tsukuyomi-chan.)

■ Kêu gọi hoặc phản đối một quan điểm chính trị, tôn giáo hoặc hệ tư tưởng cụ thể.

■ Tiết lộ nội dung khiêu khích cao độ mà không có ranh giới.

■ Công khai theo cách cho phép người khác sử dụng cho mục đích thứ cấp (như tài liệu).
*Phân phối và bán như tác phẩm nghệ thuật để tôn vinh.
