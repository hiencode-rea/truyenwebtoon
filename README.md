# Dùng cấu trúc file của dự án Thế Giới Khí

Dự án là một thư mục `the-gioi-khi/` chứa toàn file markdown. Mỗi thứ trong truyện có một file riêng: mỗi luật sức mạnh, mỗi phe, mỗi địa điểm, mỗi thuật ngữ, sau này là mỗi nhân vật và mỗi chương. Làm vậy để tìm nhanh, sửa một chỗ là xong, và không bị mâu thuẫn giữa các phần.

## Mở dự án

Giải nén `the-gioi-khi.zip` rồi mở thư mục bằng VS Code hoặc bất kỳ trình soạn thảo nào đọc được markdown. Mỗi file có hai phần. Khối nằm giữa hai dòng `---` ở đầu file là dữ liệu (tên, loại, liên kết). Phần bên dưới là nội dung viết.

Nên đọc theo thứ tự này lần đầu: `story.md` cho biết truyện nói về gì, `worldbuilding/_index.md` tóm tắt thế giới trong một đoạn, rồi mới đến các file trong `worldbuilding/systems/`.

```
the-gioi-khi/
├─ story.md                hồ sơ truyện
├─ style-sheet.md          văn phong, chính tả
├─ worldbuilding/
│  ├─ systems/             luật sức mạnh, chủng tộc, giấy phép, cấp bậc
│  ├─ factions/            chính quyền, gia tộc, hội mạo hiểm
│  ├─ locations/           năm vành đai
│  └─ artifacts/           vật phẩm (chưa có)
├─ glossary/terms/         từ ngữ riêng của thế giới
├─ characters/             nhân vật (chưa có)
├─ plot/                   cốt truyện, dòng thời gian (chưa có)
├─ scenes/, chapters/      cảnh và chương (chưa có)
└─ continuity/             ghi nhớ để các chương không lệch nhau
```

## Muốn tra gì thì mở file nào

- Khí bậc 4 làm được gì, hồi Khí ra sao: `worldbuilding/systems/pho-khi-phap.md`
- Chiêu và nhánh của kiếm, đao, cung, võ, thương, khinh, thể: `ky-nang.md`
- Ma pháp cấp mấy, hệ nào khắc hệ nào, Pháp Trận Tạm khác rune thế nào: `ma-phap.md`
- Rune còn lại những gì: `nghe-rune.md`. Máy móc: `co-gioi.md`. Tinh thạch và Say Ma: `tinh-thach.md`
- Giấy phép, vũ khí được mang, vùng được vào: `hanh-chung.md`
- Gia tộc truyền kỹ năng ra sao, Ấn Đậm hay Nhạt, người ngoài học được đến đâu: `di-truyen-huyet-an.md`
- Hạng Mạo Hiểm, Khí Giai, Đẳng Gia Tộc: `he-cap-bac.md`
- Ngoại hình, tuổi, Thiên Phú của một chủng tộc: `chung-toc-<tên>.md`. Chuyện con lai: `chung-toc.md`
- Chi trong gia tộc được tự quyết việc gì: `worldbuilding/factions/gia-toc.md`
- Vùng nào nguy hiểm cỡ nào, mật độ Ma Lực ra sao: `worldbuilding/locations/`
- Một từ viết hoa hay thường, nghĩa là gì: `glossary/terms/<từ>.md`
- Bí ẩn xuyên suốt và những gì được phép để mở: `doan-giai.md`

## Mỗi luật có một nhà

Một luật chỉ nằm đầy đủ ở một file. Các file khác chỉ nhắc ngắn rồi trỏ về. Vài ví dụ: quy tắc Hành Chứng nằm ở `hanh-chung.md`, quy tắc Huyết Ấn ở `di-truyen-huyet-an.md`, quyền hạn của Chi ở `gia-toc.md`. Chức nghiệp đặc trưng và chức nghiệp trái hướng thì nằm ở file của từng chủng tộc.

Khi đổi luật, sửa ở file gốc trước. Sau đó tìm tên luật trong cả thư mục (trong VS Code là Ctrl+Shift+F) để sửa những chỗ nhắc lại. Nếu không làm bước này, truyện sẽ có hai bản luật khác nhau.

## Khi viết một chương

Trước khi viết, mở các file mà cảnh sẽ đụng tới. Cảnh đánh nhau thì cần `pho-khi-phap.md` và `ky-nang.md`. Cảnh ở Hoang Dã thì cần `hoang-da.md` và `tinh-thach.md`. Nhân vật nào xuất hiện thì mở file của họ trong `characters/` khi đã có.

Trong lúc viết, hễ nghĩ ra tên hay khái niệm mới thì thêm ngay một file vào `glossary/terms/`, để lần sau gọi cùng một cách.

Viết xong, ghi vào `continuity/state.md` những thứ chương sau cần nhớ: ai bị thương, ai biết bí mật nào, đồ vật nằm ở đâu. Cách ghi chi tiết nằm trong skill `revision-continuity`.

## Thêm thứ mới

Địa điểm, phe, hệ thống và thuật ngữ: sao chép một file cùng loại có sẵn rồi đổi nội dung. Địa điểm lấy `noi-vuc.md` làm mẫu, phe lấy `hoi-mao-hiem.md`, hệ thống lấy `ma-phap.md`, thuật ngữ lấy `khi.md`. Giữ nguyên tên các dòng trong khối dữ liệu đầu file, chỉ đổi giá trị.

Tên file viết thường, không dấu, nối bằng gạch ngang, ví dụ `thuy-cu.md`. Các liên kết trong dự án trỏ bằng đúng tên file bỏ đuôi `.md`. Ví dụ dòng `controlled-by: chinh-quyen` trỏ tới `factions/chinh-quyen.md`. Đổi tên file thì phải đổi cả những chỗ trỏ tới nó.

Nhân vật: tạo file trong `characters/` theo mẫu của skill `character-management`, vì dự án chưa có file nhân vật nào để sao chép. Nếu nhân vật thuộc một phe hay sống ở một địa điểm, thêm tên họ vào danh sách `members` của phe đó hoặc `notable-characters` của địa điểm đó.

## Những chỗ không sửa tay

Các bảng trong mọi file `_index.md` (danh sách địa điểm, hệ thống, phe, nhân vật, chương) do lệnh `story reindex .` tạo ra, nên đừng thêm dòng bằng tay. Hiện các bảng này còn trống vì chưa chạy lệnh đó. Phần World Overview ở đầu `worldbuilding/_index.md` thì sửa tay được.

## Còn để trống

Chưa có nhân vật, cốt truyện, cảnh và chương. Các giá trị trong `story.md` như tên truyện, ngôi kể, thì và premise là giả định lúc dựng dự án, bạn cứ sửa thẳng. Trong tài liệu thiết kế còn bốn chỗ để mở: nguồn gốc Huyết Ấn, tên các gia tộc lớn, mối liên hệ giữa Rune và Đoạn Giai, và việc có Việt hóa tên Phantom hay không. Những mục ghi (Đề xuất) cũng chưa chốt.

## Sao lưu

Thư mục đã có sẵn `.gitignore`. Chạy `git init` một lần, sau mỗi buổi viết thì `git commit`, bạn sẽ lùi được về bản cũ khi lỡ sửa hỏng một luật.
