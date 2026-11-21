# Đề cương nghiên cứu cuối kỳ CS2205

**Nguyễn Xuân Dương — MSHV 26848050 — Lớp CS2205**

## Đề tài

Đánh giá khả năng khái quát hóa của mô hình học sâu đa phương thức trong trích xuất thông tin hóa đơn có bố cục chưa gặp.

Evaluating Multimodal Deep Learning for Information Extraction from Invoices with Unseen Layouts.

Đề cương tập trung vào số hóa đơn, ngày lập và tổng tiền. Hướng ứng dụng là bước trích xuất dữ liệu trước khi đối chiếu chứng từ trong TIPA 3-Ways Matching. Thực nghiệm dự kiến sử dụng DocILE; không đưa tài liệu hoặc mã nguồn nội bộ TIPA vào kho này.

## Trạng thái

Đang hoàn thiện đề cương, slide và poster theo mẫu môn học. Các file PDF và video sẽ được bổ sung sau khi kiểm tra. Đây là kế hoạch nghiên cứu; chưa có kết quả thực nghiệm của đề tài.

## Phương pháp dự kiến

So sánh checkpoint tác vụ RoBERTa và LayoutLMv3 do DocILE phát hành trên các nhóm bố cục có mức độ xuất hiện khác nhau trong tập huấn luyện. Khảo sát thêm ảnh mờ và ảnh giảm độ phân giải với hai chế độ: giữ nguyên OCR và chạy lại cùng một OCR trên cả ảnh gốc lẫn ảnh biến đổi. Đánh giá định vị trường bằng AP, bổ sung F1 và độ khớp văn bản. Chênh lệch giữa kiến trúc được diễn giải ở cấp hệ thống, không quy riêng cho đặc trưng thị giác.

## Tài liệu nền

- Yupan Huang, Tengchao Lv, Lei Cui, Yutong Lu, Furu Wei: LayoutLMv3: Pre-training for Document AI with Unified Text and Image Masking. ACM Multimedia 2022: 4083-4091. [Bài báo](https://doi.org/10.1145/3503161.3548112).
- Štěpán Šimsa, Milan Šulc, Michal Uřičář, Yash Patel, Ahmed Hamdi, Matěj Kocián, Matyáš Skalický, Jiří Matas, Antoine Doucet, Mickaël Coustaty, Dimosthenis Karatzas: DocILE Benchmark for Document Information Localization and Extraction. ICDAR (3) 2023: 147-166. [Bài báo](https://arxiv.org/abs/2302.05658), [mã nguồn và dữ liệu](https://github.com/rossumai/docile).
- Yufan Chen, Jiaming Zhang, Kunyu Peng, Junwei Zheng, Ruiping Liu, Philip Torr, Rainer Stiefelhagen: RoDLA: Benchmarking the Robustness of Document Layout Analysis Models. CVPR 2024: 15556-15566. [Bài báo](https://arxiv.org/abs/2403.14442).
