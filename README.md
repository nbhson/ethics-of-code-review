# Ethics of Code Review

## What are the ethics of Code Review?

### Represent yourself - Đại diện cho bản thân

Khi bạn review code của đồng nghiệp, thật khó để quyết định cách giải quyết một số khối code khó hiểu. Nó có thể không gây nhầm lẫn cho người khác để có thể hiểu nó, nhưng cần phải làm rõ một số điều.

> Hãy sử dụng "Tôi" để chỉ ra rằng đó là ý kiến ​​​​của bạn không bắt buộc đối với bất kỳ ai khác.

**Good Examples:**

`I can't understand this code block, could you please explain what's the purpose behind?`

`I am confused about the reason this line of code is placed here?`

**Instead of:**

`This code block is not understandable`

`This code block is so confusing`

### Adding some rationale - Thêm một số lí do

Khi bạn đọc code, phát hiện ra code này mô tả hành vi chưa đúng hoặc bỏ lỡ điều gì đó phải được giải quyết.

> Bạn nên thêm một số lý do bên cạnh comment sẽ làm cho nó như một sự chắc chắn. Vì vậy, chuẩn bị cho những lý do tại sao bạn nghĩ về comment

**Good Examples:**

`This Code isn't connected to backend and will fail eventually, as the backend service start function not called`

**Instead of:**

`This Code isn't connected to backend and will fail eventually`

### Question not Demand - Câu hỏi không yêu cầu

Đặt câu hỏi là chìa khóa để bắt đầu cuộc trò chuyện giữa người review và author.

> Nó không chỉ quan trọng đối với code hiện tại đang được review mà còn đối với bất kỳ sửa đổi nào trong tương lai.

**Good Examples:**

`Could you check the issue of closing the connection after successfully read data from the server?`

**Instead of:**

`You've not closed the connection after reading from the server`

### Propose a value - Đề xuất một giá trị

Mục đích ban đầu của việc review code là để cải thiện, do đó code hoạt động tốt hơn cho tất cả những người đóng góp.

> Suy nghĩ về giá trị mà bạn phải cân nhắc nếu, chẳng hạn như ngữ cảnh đang thúc đẩy một bản sửa lỗi, tập trung vào chính tả sẽ không phải là giá trị tốt nhất mà bạn thêm vào đây, thay vào đó, đề xuất một bước kiểm tra chính tả trong tương lai sẽ tạo ra nhiều giá trị hơn.

**Good Examples:**

`What about adding a spell checker to be integrated into the IDE <IDE name > to check to misspell?`

`Can we add a code formatter step?`

**Instead of:**

Adding multiple time:

`Please fix typos` or `Fix the misspelling in all code changes`

### Don't make fun of code - Đừng chế diễu code

Trong mọi trường hợp, nó không phải là một giá trị tích cực. Vì vậy, việc loại bỏ những lời lẽ mỉa mai khi review code sẽ loại bỏ mọi cảm xúc tiêu cực khỏi phản hồi được gửi.

**Good Examples:**

`I believe this code block can be written in a more functional way, what do you think ?`

**Instead of:**

`This code block miss the professional hands`

### Be objective - Hãy khách quan

Khi bạn thực sự thấy có vấn đề trong một số thay đổi về code, hãy giải quyết vấn đề đó bằng code chứ không phải bởi người viết nó, bằng cách này, bạn đang review một đoạn code do người đã viết nó mà không dựa vào kiến ​​thức chuyên môn nào đó của chủ author.

**Good Examples:**

`Could you check the issue of closing the connection after successfully read data from the server?`

`This code is missing the failed connection error handling, could you check please ?`

**Instead of:**

`You've not closed the connection after reading from the server`

`You should handle the failed connection error`

### Avoid judgemental words - Tránh những từ phán xét

Lời nói chỉ về sự tôn trọng giữa các thành viên trong một dự án. Khi review code, ngôn ngữ cơ thể, nét mặt và cảm xúc không xuất hiện trong giao tiếp bằng văn bản, vì vậy hãy tránh các cụm từ như "Thật dễ dàng", "Không mất thời gian", "Đó là một nhiệm vụ tầm thường" và "Điều đó rõ ràng trong code " và cố gắng diễn đạt lại chúng theo cách thoải mái hơn sẽ xây dựng mối quan hệ học hỏi lẫn nhau giữa tác giả code và người đánh giá.

**Good Examples:**

`I believe function ABC can provide same functionality could you check it please?`

`What about developing a new approach that utilizes remote connection?`

**Instead of:**

`Function XYZ is obviously the same as ABC`

`Please develop a new approach for remote connection, it's just easy to break this one`

### Be aware of the author context - Nhận biết bối cảnh của tác giả

Khi review một số thay đổi code, bạn phải review bối cảnh của tác giả code, anh ấy/cô ấy có phải là nhân viên mới không? thêm một hotfix một cách nhanh chóng? từ đội khác? hoặc đẩy một số thay đổi kiến ​​trúc?.

**Good Examples:**

`It seems this function missed linting, Could you please check our team coding guidelines?`

`[Hotfix]: In order not to have this issue again, what about adding a flag for function XYZ to enable/disable using it?`
**Instead of:**

`Linting functions is a must in our team philosophy`

`[Hotfix]: This fix is missing proper naming for branches`

### Don't play the instructor role! - Đừng đóng vai là người hướng dẫn (ra lệnh)

Hãy đặt một cuộc trò chuyện ở chế độ tìm hiểu và khám phá để cả tác giả code và reviewer (bạn) khám phá miền vấn đề mà code thay đổi để giải quyết và tìm hiểu các cách giải quyết mới.

**Good Examples:**

`It might be a good idea to segregate this interface into multiple ones to avoid fat interfaces syndrome`

**Instead of:**

`Segregate this interface to multiple ones, we don't want fat interfaces to leak to our codebase`

### Expect misunderstandings - Mong đợi sự hiểu lằm

Khi review code của các nhà phát triển khác từ một nhóm khác hoặc thậm chí từ các thành viên trong nhóm của bạn, mong đợi sự hiểu lầm có thể phát sinh do chênh lệch về thâm niên, kinh nghiệm, phạm vi công việc hoặc sở thích cá nhân.

> Trong trường hợp này, tránh những từ gay gắt hoặc chỉ trích và yêu cầu diễn đạt lại hoặc chỉ ra lý do thay đổi code sẽ giúp cả hai bên xây dựng đánh giá code đáng tin cậy để truyền bá văn hóa đánh giá code.

**Good Examples:**

`What about re-phrasing this function to be simpler and more readable ?`

**Instead of:**

`I can't understand what this code does... totally confused!`

## Các bước review code

- B1: Cú pháp code & Grammar
- B2: Tính sử dụng lại code và lỗi trùng lặp code
- B3: Chất lượng kỹ thuật
  - Code Logic:
    Code có đạt hiệu năng như mô tả không? Các tính năng có hoạt động như mong muốn không? Logic của code có thoả mãn không? Nếu chỉ nhìn code thì không đủ để xác minh chúng, hãy kiểm tra các nhánh liên quan và nhìn rộng ra để tìm ra lựa chọn tốt.
  - Quy ước đặt tên (Naming Convention):
    Có các file hay class và phương thức nào được mô tả tốt chưa? Những tên đó có đúng mục đích không? Nó có dễ hiểu không? Các tên object, class có đúng theo chức năng của nó? Các hằng số có được sử dụng khi cần và giá trị của nó không thay đổi chứ? Code có tuân theo quy tắc đặt tên không? Theo cú pháp lặc đà (Camel) hay dạng gách chân (underscore)?
  - Cô đọng Code:
    Có biến nào không được sử dụng hoặc đoạn code nào không được sử dụng không? Có biến nào được gán mà chỉ được dùng 1 lần không? Có thể giảm số dòng code lại không? Ví dụ dùng toán tử 3 ngôi thay vì dùng if else.
  - ...

## Một số câu hỏi dưới đây sẽ là công cụ rất tốt giúp bạn cải thiện quá trình review của mình:

- Tôi có gặp khó khăn trong việc hiểu code này không?
- Có phần nào quá phức tạp cần refactor lại không?
- Code này đã được sắp xếp hợp lý trong cấu trúc thư mục chưa?
- Class name có trực quan và có đúng với chức năng không?
- Có class nào quá lớn không?
- Có phương thức nào quá dài không?
- Các tên phương thức có rõ ràng và trực quan không?
- Đã viết đủ document cho các phần code cần chưa (như viết doc cho API chẳng hạn)?
- Code đã được test kỹ chưa?
- Có cách nào làm cho code trở nên hiệu quả hơn không?
- Code có đúng với quy chuẩn của team không?

## Link

- <https://dev.to/_meseery/ethics-of-code-review-3f66>
