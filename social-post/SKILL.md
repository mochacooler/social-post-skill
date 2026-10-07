---
name: social-post
description: Viết social post (Facebook/LinkedIn, mặc định tiếng Việt) có kiểm chứng dữ kiện, kèm infographic tối giản dễ đọc trên điện thoại. Dùng skill này mỗi khi người dùng nhắc viết post, bài đăng, social posting, caption, explainer, "biến phân tích/kết quả/quy định này thành bài đăng", hoặc cần ảnh infographic cho bài, kể cả khi họ không nói chữ "social". Đặc biệt hợp với chủ đề Finance, thuế, vận hành, AI, nơi độ tin cậy quan trọng hơn lượt xem.
---

# Social Post: viết bài có căn cứ + infographic tối giản

Skill này đúc kết từ một quy trình thực tế: viết bài Facebook giải thích cách Anthropic tính VAT cho Claude tại Việt Nam, đi qua nhiều vòng phản biện về căn cứ pháp lý và hai vòng chỉnh infographic. Mục tiêu là tái dùng những gì đã làm đúng và tránh những lỗi đã gặp.

## Vì sao quy trình này tồn tại

Người đọc chính là đồng nghiệp, chuyên gia và đối tác của tác giả. Một con số sai hoặc một điều luật đã hết hiệu lực làm mất uy tín nhiều hơn mười bài post hay mang lại. Vì vậy thứ tự luôn là: **kiểm chứng trước, framing sau, viết cuối, hình ảnh cuối cùng**. Hút view đến từ hook rõ ràng và cấu trúc dễ quét, không đến từ việc nói chắc hơn bằng chứng cho phép.

## Quy tắc không thương lượng

1. **Không bịa dữ liệu.** Không số liệu, trích dẫn, benchmark, điều luật hay case study nào mà chưa có nguồn. Thiếu dữ liệu thì dùng placeholder `[số liệu cần điền]` hoặc diễn đạt định tính. Ví dụ minh họa phải ghi rõ "minh họa", và con số phải tính được bằng công thức hiển thị.
2. **Chỉ soạn, không đăng.** Không đăng, gửi, chia sẻ ra ngoài thay người dùng. Kết quả cuối là bản nháp + ảnh để họ tự đăng.
3. **Phản biện thì luôn kèm option.** Khi thấy luận điểm yếu, rủi ro hoặc câu chữ dễ bị bắt bẻ, nêu ngắn gọn và đưa 2-3 phương án (kèm đánh đổi, một phương án đề xuất), không áp một lựa chọn duy nhất.
4. **Câu chữ người dùng đưa thì dùng nguyên văn.** Chỉ sửa lỗi chính tả hoặc định dạng số, báo lại thay đổi đó. Nếu thấy câu đó có rủi ro logic, nêu rủi ro và option bên dưới bản nháp, không tự ý thay.

## Quy trình

### 1. Nhận yêu cầu (hỏi tối đa một câu)

Cần biết: chủ đề, kênh, đối tượng đọc, mục tiêu (giải thích, thu hút thảo luận, thể hiện chuyên môn), và có sẵn tài liệu nguồn nào. Thiếu gì thì nêu giả định và làm tiếp, chỉ hỏi khi câu trả lời làm thay đổi bài. Mặc định: Facebook, tiếng Việt, 150-250 từ, tác giả nói bằng ngôi "mình".

### 2. Kiểm chứng (trước khi viết chữ nào)

Lập bảng ngắn **Facts / Assumptions / Unknowns** cho mọi mệnh đề sẽ xuất hiện trong bài. Với mỗi Fact, ghi nguồn và đã đọc nguyên văn hay chỉ qua bản tóm tắt. Nguồn qua summarizer là bằng chứng yếu hơn văn bản gốc, và phải được gắn nhãn như vậy.

Với trích dẫn pháp lý, quy định hoặc chuẩn mực:
- **Kiểm tra hiệu lực**: văn bản nào đang có hiệu lực ở ngày hôm nay, văn bản nào đã bị thay thế (tìm "thay thế", "bãi bỏ", ngày hiệu lực). Dùng văn bản mới nhất và nói rõ khi nhắc văn bản cũ. Người dùng từng phản hồi vì trích luật cũ.
- **Kiểm tra phạm vi**: điều khoản viết cho đối tượng nào. Một điều khoản đúng chữ nhưng viết cho đối tượng khác chỉ là căn cứ tham khảo, không phải căn cứ trực tiếp.
- **Kiểm tra thuế suất, tỷ lệ, định nghĩa** đi kèm cùng điều khoản, vì lệch ở đây là chỗ dễ bị bắt lỗi nhất.
- Trích nguyên văn tối đa một câu ngắn, còn lại diễn đạt lại.

Công cụ: WebSearch/WebFetch cho nguồn công khai; trình duyệt cho trang cần cuộn hoặc ảnh; nếu một nguồn bị chặn thì nói rõ và đánh dấu Unknown, không đi vòng.

Với phép tính: chạy bằng script (python), không tính nhẩm. Ghi cả phép làm tròn.

**Nếu luận điểm của người dùng yếu hơn họ nghĩ**, nói ngay ở bước này, kèm option (ví dụ: A. bài với kết luận có điều kiện, B. bài khẳng định kèm rủi ro, C. chờ xác nhận chính thức rồi mới đăng). Đề xuất phương án bám bằng chứng.

### 3. Chọn framing

- Giải thích **cơ chế**, không phán "ai đúng ai sai" khi bằng chứng chưa đủ. Dạng này vừa trung thực vừa dễ chia sẻ hơn.
- Chỉ có **một nguyên tắc** làm nền (ví dụ VAT = giá tính thuế × thuế suất). Khi hai cách tính cho kết quả khác nhau, chỉ ra chúng dùng cùng công thức và khác nhau ở một biến duy nhất. Không dựng "hai chế độ" nếu không có căn cứ cho cả hai.
- Dùng mệnh đề **"Nếu A và B thì C"** khi kết luận phụ thuộc điều kiện chưa xác nhận. Đó là cách nói chắc đến đúng mức bằng chứng.
- Tránh từ tuyệt đối ("chắc chắn", "không phải X") nếu phản ví dụ còn dễ nghĩ ra. Cách nói an toàn hơn: "không phải lỗi cộng thuế hai lần" thay cho "không phải thuế chồng thuế" khi người đọc vẫn có thể gọi hiện tượng đó bằng tên cũ.
- Hai bên của một so sánh phải được gắn nhãn đúng bản chất (đâu là cách tham chiếu, đâu là cách thực tế trên chứng từ).

### 4. Viết bài

Khung (giữ đúng thứ tự, mỗi khối ngắn):

```
[icon] Hook: nhiều người đang hiểu/hỏi X. Mình đọc nguồn thay vì đoán.

1️⃣ Điều chính chủ thể nói/ghi (trích ≤ 1 câu)
2️⃣ Điều đã xác minh được (kèm nguồn đã kiểm)
3️⃣ Căn cứ tham khảo (⚖️📄📑, mỗi mục 1 dòng: văn bản, điều, ý chính)

💡 Cách hình dung: 2-3 gạch đầu dòng so sánh, cùng một nguyên tắc
Đoạn kết luận có điều kiện (Nếu... thì...)
📊 Một con số chốt (nếu có)

⚠️ Điểm lưu ý cần xác nhận lại: những gì còn mở
📌 Dòng cá nhân + kêu gọi: "Đây là cách hiểu cá nhân tự tìm tòi... Anh chị nào nắm rõ xin góp ý giúp mình 🙏"

#Hashtag (4-6, không dấu, CamelCase)
```

Quy tắc phong cách:
- Một lời kêu gọi hành động duy nhất ở cuối. Hai CTA làm loãng nhau.
- Icon đặt ở đầu khối để quét nhanh, mỗi khối một icon, tránh rải icon giữa câu.
- Số tiền, tỷ lệ: dùng dấu phẩy thập phân kiểu Việt (`$22,22`, `11,11%`), nhất quán trong cả bài và ảnh. VND và USD ghi rõ đơn vị.
- Giữ thuật ngữ tiếng Anh chuẩn ngành (gross-up, NPL, RPC, FP&A) khi chính xác hơn bản dịch.
- Nếu bài nhắc thông tin nội bộ của công ty tác giả, hỏi lại một dòng xem họ có muốn công khai không, vì đó là quyết định của họ.
- Hook nêu hiện tượng mọi người đang thấy, không nêu kết luận. Kết luận để dành cho cuối.
- **Mệnh đề về người khác hoặc về kinh nghiệm của tác giả là dữ kiện, không phải văn phong.** "Nhiều anh chị hay hỏi", "theo kinh nghiệm của mình", "mình thường làm" chỉ dùng khi người dùng đã nói điều đó. Nếu không, viết dạng câu hỏi hoặc khung nhìn ("Câu hỏi đáng đặt ra:", "Một cách nhìn:") hoặc ghi vào danh sách giả định để họ xác nhận.
- **Không biến giả định thành câu khẳng định trong bài.** Quy trình thực tế của người dùng (ai duyệt kết quả, công cụ cụ thể, lý do chọn cách làm) mà họ chưa nói thì để trong ghi chú kèm option, không viết vào bài như sự thật.

### 5. Infographic

Làm ảnh khi bài có cơ chế, so sánh, quy trình hoặc con số. Ảnh nhắc lại phần cốt lõi, không chép lại cả bài.

**Mặc định: canvas HTML/CSS rồi chụp bằng Playwright.** Cho kiểm soát tuyệt đối typography tiếng Việt, icon, và khớp từng con số với bài. Chi tiết ở dưới.

**Tùy chọn: AntV Infographic** (`@antv/infographic`, MIT, ~270 template, SSR qua `@antv/infographic/ssr`) khi chỉ cần một khối sơ đồ chuẩn (donut, steps, funnel, quadrant, roadmap, cây). Cách dùng như một **thành phần nhúng** trong canvas HTML, không thay cả canvas. Xem mục "Dùng AntV" bên dưới. Lý do không dùng làm mặc định: font mặc định tải từ CDN bị chặn trong sandbox nên rơi về serif, kiểu mặc định nhiều màu (đối lập với yêu cầu tối giản), nhãn nhóm trong nhiều template compare không hiển thị như kỳ vọng, và bố cục khó khớp chính xác với chữ tiếng Việt dài.

#### Nguyên tắc thiết kế (rút từ phản hồi "màu mè quá")

- **Một màu nhấn duy nhất** (teal `#0E8A8A`) + navy + xám. Một màu thứ hai chỉ cho icon cảnh báo. Tối đa một dải nền tối. Không hình trang trí vô nghĩa.
- **Chữ đọc được trên điện thoại**: ảnh 1080 px hiển thị khoảng 390 px, nên hệ số 0,36. Tiêu đề ≥ 56 px, nội dung ≥ 22 px, chú thích ≥ 18 px. Chữ nhỏ hơn thì cắt bớt nội dung thay vì thu nhỏ chữ.
- **Ít chữ, có cấu trúc**: tiêu đề hỏi → trích dẫn nguồn → quy tắc một dòng → so sánh 2 cột → con số chốt → căn cứ (3 thẻ) → đã xác minh / cần xác nhận → câu miễn trừ.
- **Icon nét đồng bộ** từ Lucide (`npm i lucide-static`), nhúng inline SVG, `stroke: currentColor`. Gợi ý: `receipt quote calculator landmark percent scale file-text scroll-text badge-check triangle-alert`.
- Tỷ lệ **4:5, 1080×1350** cho feed Facebook (cao hơn sẽ bị cắt). Xuất ở `device_scale_factor=2`.
- Ảnh phải khớp bài đến từng con số và từng thuật ngữ. Nếu bài có câu "Cần xác nhận lại", ảnh phải có dải tương ứng.

#### Thư mục build riêng cho từng bài

Mỗi bài dùng một thư mục build riêng đặt theo slug chủ đề (ví dụ `/tmp/social-post-chot-so/`), chứa `fonts.css`, `node_modules`, HTML và PNG. Không dùng một đường dẫn tạm chung: khi nhiều bài hoặc nhiều subagent chạy song song, chúng ghi đè lên nhau và ảnh giao ra sai chủ đề (đã xảy ra khi kiểm thử). Sau lần render cuối, mở ảnh và xác nhận đúng chủ đề rồi mới sao chép vào thư mục giao hàng; đồng thời chép cả `fonts.css` hoặc nhúng font base64 để HTML mở lại ở nơi khác vẫn đúng font.

#### Font: không dựa vào Google Fonts

Sandbox thường không tới được CDN font. Dùng gói npm (registry thường được phép):

```bash
npm i @fontsource/montserrat lucide-static
```

Chỉ lấy ba subset `vietnamese`, `latin-ext`, `latin` ở các weight 400/600/700/800 và sinh `fonts.css` trỏ `file://` tới các file `.woff2`. Dùng weight 600 thật (đừng khai báo 500 mà không nạp file, trình duyệt sẽ rơi về font khác). Dự phòng: `'DejaVu Sans'` (có sẵn, hỗ trợ tiếng Việt).

```python
import re, os
base = os.path.abspath('node_modules/@fontsource/montserrat')
out = []
for w in (400, 600, 700, 800):
    css = open(f'{base}/{w}.css').read()
    for m in re.finditer(r'/\*\s*montserrat-(\S+?)-\d+-normal\s*\*/\s*(@font-face\s*\{.*?\})', css, flags=re.S):
        name, b = m.groups()
        if name in ('vietnamese', 'latin-ext', 'latin'):
            b = re.sub(r"url\(\./files/([^)]+\.woff2)\) format\('woff2'\), url\([^)]+\) format\('woff'\)",
                       lambda mm: f"url(file://{base}/files/{mm.group(1)}) format('woff2')", b)
            out.append(b)
open('fonts.css', 'w').write('\n'.join(out))
```

#### CSS khởi đầu (token + thành phần)

```css
:root{--navy:#1B2440;--gray:#5B6478;--soft:#F4F6FA;--line:#E3E7EF;
      --acc:#0E8A8A;--acc-l:#E4F3F3;--amber:#D98A00}
*{box-sizing:border-box;margin:0;padding:0}
html,body{width:1080px;height:1350px;background:#fff;color:var(--navy);
  font-family:'Montserrat','DejaVu Sans',sans-serif;-webkit-font-smoothing:antialiased}
svg.ic{width:1em;height:1em;stroke:currentColor;fill:none;stroke-width:2;
  stroke-linecap:round;stroke-linejoin:round;flex:none}
.canvas{width:1080px;height:1350px;padding:60px 60px 40px;display:flex;flex-direction:column;gap:30px}
h1{font-size:62px;font-weight:800;line-height:1.1} h1 span{color:var(--acc)}
.quote{display:flex;gap:16px;align-items:center;background:var(--soft);border-radius:18px;padding:18px 22px;font-size:25px;font-weight:600}
.cmp{display:grid;grid-template-columns:1fr 1fr;gap:20px}
.box{border:2px solid var(--line);border-radius:22px;padding:22px 24px 12px;position:relative}
.box.hl{border-color:var(--acc);background:var(--acc-l)}
.row{display:flex;justify-content:space-between;align-items:baseline;padding:14px 0;border-top:1px solid var(--line)}
.row .l{font-size:24px;font-weight:600} .row .v{font-size:38px;font-weight:800;white-space:nowrap}
.eff{display:flex;align-items:center;gap:22px;border-radius:20px;background:var(--navy);color:#fff;padding:22px 28px}
.law{display:grid;grid-template-columns:repeat(3,1fr);gap:16px}
.law div{background:var(--soft);border-radius:16px;padding:14px 16px}
.st{display:flex;gap:14px;align-items:flex-start;font-size:22px;font-weight:600;line-height:1.35}
.foot{margin-top:auto;font-size:18px;font-weight:600;color:var(--gray);text-align:center}
```

Sinh HTML từ một template có placeholder `{{icon:ten}}`, thay bằng inline SVG đọc từ `node_modules/lucide-static/icons/<ten>.svg`, để icon luôn đồng bộ nét.

#### Chụp ảnh và kiểm tra

```python
from playwright.sync_api import sync_playwright
import os
with sync_playwright() as pw:
    b = pw.chromium.launch()
    pg = b.new_page(viewport={'width':1080,'height':1350}, device_scale_factor=2)
    pg.goto('file://' + os.path.abspath('infographic.html'))
    pg.wait_for_load_state('networkidle'); pg.evaluate('document.fonts.ready')
    last = pg.evaluate("""()=>{const k=[...document.getElementById('canvas').children]
      .filter(e=>!e.classList.contains('deco'));return k[k.length-1].getBoundingClientRect().bottom}""")
    print('last bottom', last)   # phải <= 1320
    pg.screenshot(path='infographic.png'); b.close()
```

Sau khi chụp **luôn mở ảnh bằng Read để nhìn thật** trước khi gửi. Kiểm tra: chữ không tràn hay bị cắt, không có từ mồ côi ở cuối dòng (dùng `<span style="white-space:nowrap">` cho cụm như "(1 − tỷ lệ %)"), dấu tiếng Việt đúng, số khớp bài, không còn khoảng trống lớn ở đáy (nếu có thì tăng cỡ chữ hoặc giãn khoảng cách thay vì để trống).

Lỗi đã gặp, nên tránh ngay từ đầu:
- Selector `.canvas>*{position:relative}` đè lên `.deco{position:absolute}`, khiến hình trang trí chiếm chỗ trong luồng flex và đẩy nội dung tràn. Dùng `.canvas>*:not(.deco)` hoặc bỏ hình trang trí.
- `scrollHeight` của canvas lớn hơn 1350 do phần tử trang trí tràn ra ngoài vẫn có thể ổn; đo bằng `bottom` của khối cuối.

#### Dùng AntV (tùy chọn, khi cần một khối sơ đồ chuẩn)

```bash
npm i @antv/infographic
```
```js
import { renderToString } from '@antv/infographic/ssr';
const svg = await renderToString(`
infographic chart-pie-donut-plain-text
theme
  palette #0E8A8A #F59E0B
data
  title Cơ cấu số tiền khách trả
  items
    - label Giá niêm yết
      value 20
    - label VAT
      value 2.22
`, { width: 900, height: 560 });
```
- Cú pháp: dòng đầu `infographic <template>`, thụt hai khoảng trắng, `key value`, mảng bằng `-`. Khối `theme` với `palette` đổi màu được (đã kiểm chứng).
- Dữ liệu: `items` (list/chart), `sequences` (steps), `compares` (so sánh, hai nút gốc cho `compare-binary-*`).
- Template tiêu biểu: `chart-pie-donut-plain-text`, `sequence-steps-simple`, `sequence-funnel-simple`, `sequence-roadmap-vertical-plain-text`, `compare-quadrant-*`, `list-grid-*`.
- SVG nhận font theo trình xem, nên khi chụp phải nhúng SVG vào trang đã nạp `fonts.css`. Thư viện in cảnh báo "font not registered" khi đo chữ; layout dùng số liệu dự phòng nên cần xem ảnh thật và chỉnh `width/height`.
- Luôn kiểm tra ảnh. Nếu template không hiển thị đúng nhãn hoặc quá nhiều màu, quay về canvas HTML.

### 6. QA trước khi giao

- Mọi con số trong bài và ảnh khớp nhau và khớp phép tính đã chạy.
- Mọi điều khoản được trích đúng hiệu lực, đúng phạm vi, có nhãn mức chắc chắn nếu chỉ đọc qua nguồn thứ cấp.
- Không còn từ tuyệt đối ngoài những chỗ có bằng chứng trực tiếp.
- Bài có đúng một CTA, hashtag ở cuối, icon ở đầu khối.
- Ảnh đã được nhìn bằng mắt sau lần render cuối.

### 7. Giao kết quả

Gửi ảnh bằng công cụ gửi file, và đưa bài nháp trong khung code để dễ chép. Phần giải thích ngắn gồm: những gì thay đổi so với yêu cầu, một đến hai điểm đáng cân nhắc kèm option, và bước tiếp theo. Nhắc rõ rằng bài chỉ là bản nháp và việc đăng do người dùng quyết định. Nếu có chủ đề tư vấn chuyên môn (thuế, pháp lý, tài chính), thêm một dòng nêu rõ đây không phải tư vấn chuyên môn.

## Khi người dùng phản hồi

- "Màu mè quá", "rối quá": giảm màu, cắt khối, tăng cỡ chữ, bỏ trang trí. Đừng thêm.
- "Thêm icon": dùng Lucide nét đồng bộ, không dùng emoji trong ảnh (emoji lệch phong cách và phụ thuộc font hệ thống).
- Người dùng gửi câu chữ thay thế: dùng nguyên văn (quy tắc 4), điều chỉnh các phần còn lại cho khớp, rồi báo lại.
- Người dùng phản biện logic: xem lại bằng chứng thật sự, đừng bảo vệ lập luận cũ. Thừa nhận phần đúng, nêu phần còn mở, đưa option.
