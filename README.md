# ProxyChangerPC Update Channel

Repository công khai chỉ dùng cho cập nhật online của Proxy Changer Pro PC.

## Không đưa source vào repo này

Chỉ lưu `version.json` và GitHub Release assets (`ProxyChangerPro_vX.Y.Z.exe`).

## Manifest

`version.json` dùng các trường:

- `version`: phiên bản mới nhất, ví dụ `1.21.2`
- `url`: link tải trực tiếp EXE của GitHub Release
- `sha256`: SHA256 của chính file EXE phát hành
- `mandatory`: `true` nếu bắt buộc cập nhật
- `notes`: ghi chú phiên bản

## Quy trình phát hành

1. Chốt và test source.
2. Bảo vệ/mã hóa source nếu cần.
3. Build EXE final.
4. Tính SHA256 của EXE final.
5. Tạo GitHub Release và upload EXE.
6. Cập nhật `version.json` sau cùng bằng version, URL và SHA256 đúng của release.

Không cập nhật manifest trước khi asset release đã tải được và checksum đã xác nhận.
