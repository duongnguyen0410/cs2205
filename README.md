# Đề cương nghiên cứu cuối kỳ CS2205

**Nguyễn Xuân Dương — MSHV 26848050 — Lớp CS2205**

## Đề tài

Đánh giá khả năng khái quát hóa của mô hình học sâu đa phương thức trong trích xuất thông tin hóa đơn có bố cục chưa gặp.

Evaluating Multimodal Deep Learning for Information Extraction from Invoices with Unseen Layouts.

Đề cương đánh giá ba trường cấp chứng từ và năm loại trường dòng hàng trên chứng từ dạng hóa đơn của DocILE. Các trường tiền là số gồm thuế. Hướng ứng dụng là bước trích xuất trước khi đối chiếu chứng từ trong TIPA 3-Ways Matching. Đối chiếu ba bên vẫn là việc sau. Không đưa tài liệu hoặc mã nguồn nội bộ TIPA vào kho này.

| Nhóm | Ý nghĩa | Mã DocILE |
| --- | --- | --- |
| Cấp chứng từ | Số chứng từ | `document_id` |
| Cấp chứng từ | Ngày lập | `date_issue` |
| Cấp chứng từ | Tổng gồm thuế | `amount_total_gross` |
| Trường dòng hàng | Mô tả hàng hóa, dịch vụ | `line_item_description` |
| Trường dòng hàng | Số lượng | `line_item_quantity` |
| Trường dòng hàng | Đơn vị tính | `line_item_units_of_measure` |
| Trường dòng hàng | Đơn giá gồm thuế | `line_item_unit_price_gross` |
| Trường dòng hàng | Thành tiền dòng gồm thuế | `line_item_amount_gross` |

## Trạng thái

Bản native đã được duyệt và xuất: đề cương 5 trang A4, thuyết trình 10 trang, poster A3 dọc 1 trang. Ba PDF trong kho là đúng các bản xuất đó. Đây là đề cương, chưa có kết quả thực nghiệm. Số buổi vắng: 0. Câu hỏi QT cá nhân/nhóm: 0/0. Ảnh cá nhân, video YouTube và tự đánh giá chưa có. Tác giả tự hoàn tất tệp AIO và nộp Classroom.

## Tài liệu

| Tài liệu | PDF | Bản Google |
| --- | --- | --- |
| Đề cương | [CS2205.DeCuong.pdf](CS2205.DeCuong.pdf) | [Google Docs](https://docs.google.com/document/d/1WnFf4SAejPqYltruMU51x1uZtL8euG0ALZFIhETykxE/edit) |
| Thuyết trình | [CS2205.Slide.pdf](CS2205.Slide.pdf) | [Google Slides](https://docs.google.com/presentation/d/1TN0B9FNN4McuKkSjm35u-gw2U5DRVeZAClajPaJVJ_U/edit) |
| Poster | [CS2205.Poster.pdf](CS2205.Poster.pdf) | [Google Slides](https://docs.google.com/presentation/d/159lwOmHgG-HgZNTs42EH_rlmtl-m6WjNh3qDIhPxeRk/edit) |

[Kịch bản video theo 10 slide](KichBanVideo.txt). Cần đọc thử và bấm giờ để video không quá 5 phút.

Slide 3 dùng panel trái của Hình 1 DocILE, Šimsa và cộng sự (2023), [nguồn](https://arxiv.org/html/2302.05658v2), thu nhỏ đúng tỉ lệ. Slide mô hình dùng toàn bộ Hình 3 LayoutLMv3, Huang và cộng sự (2022), [nguồn](https://arxiv.org/html/2204.08387v3), thu nhỏ đúng tỉ lệ, theo [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/). Sơ đồ dữ liệu và bảng minh họa là hình tự vẽ; số trong bảng là ví dụ.

## Phương pháp dự kiến

So sánh checkpoint tác vụ RoBERTa và LayoutLMv3 do DocILE phát hành. Bộ gán trường của RoBERTa chỉ dùng văn bản OCR. Ghép dòng dùng nhãn NER dự đoán và hình học hộp OCR, với cấu hình gộp cố định. LayoutLMv3 thêm vị trí và ảnh. Khảo sát ảnh gốc, ảnh mờ Gaussian và ảnh giảm độ phân giải. Chế độ A giữ token và hộp OCR. Chế độ B chạy lại DocTR rồi cấp cùng OCR cho hai mô hình. Chỉ số chính tách đôi: AP định vị cho ba trường cấp chứng từ và micro-F1 cho năm loại trường dòng hàng, gồm gán dòng.

## Tài liệu nền

- Yupan Huang, Tengchao Lv, Lei Cui, Yutong Lu, Furu Wei: LayoutLMv3: Pre-training for Document AI with Unified Text and Image Masking. ACM Multimedia 2022: 4083-4091. [Bài báo](https://doi.org/10.1145/3503161.3548112).
- Štěpán Šimsa, Milan Šulc, Michal Uřičář, Yash Patel, Ahmed Hamdi, Matěj Kocián, Matyáš Skalický, Jiří Matas, Antoine Doucet, Mickaël Coustaty, Dimosthenis Karatzas: DocILE Benchmark for Document Information Localization and Extraction. ICDAR (3) 2023: 147-166. [Bài báo](https://arxiv.org/abs/2302.05658), [mã nguồn và dữ liệu](https://github.com/rossumai/docile).
- Yufan Chen, Jiaming Zhang, Kunyu Peng, Junwei Zheng, Ruiping Liu, Philip Torr, Rainer Stiefelhagen: RoDLA: Benchmarking the Robustness of Document Layout Analysis Models. CVPR 2024: 15556-15566. [Bài báo](https://arxiv.org/abs/2403.14442).
