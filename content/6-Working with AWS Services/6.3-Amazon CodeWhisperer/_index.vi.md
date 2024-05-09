---
title : "Amazon CodeWhisperer"
date :  "`r Sys.Date()5" 
weight : 3
chapter : false
pre : " <b> 6.3 </b> "
---

#### Sử dụng CodeWhisperer để viết mã nhanh hơn

CodeWhisperer có thể được sử dụng như một công cụ tự động hoàn chỉnh siêu mạnh mẽ, giúp giảm đáng kể việc gõ phím khi viết từng dòng hoặc khối mã. Để sử dụng CodeWhisperer theo cách này, chỉ cần viết mã như bạn đã làm trước đây. CodeWhisperer sẽ đưa ra các gợi ý tự động khi bạn gõ. Chấp nhận các gợi ý khi chúng hữu ích và bỏ qua chúng khi chúng không phù hợp. Theo kinh nghiệm của tôi, việc sử dụng CodeWhisperer theo cách này một mình đã giảm việc gõ phím của tôi đi 50% hoặc hơn.

#### Tạo Hàm Tự Động

Trong lập trình, việc tạo ra các hàm có thể tự động sinh ra nội dung từ các chữ ký là một phần quan trọng của quá trình phát triển phần mềm. Các lập trình viên tài năng thường sử dụng các tên rõ ràng, mô tả cho các hàm và tham số của họ. Nếu bạn tuân thủ thực hành này trong lập trình của riêng bạn, CodeWhisperer sẽ có đủ ngữ cảnh để triển khai nhiều hàm cho bạn.

Khi bạn nhập chữ ký hàm dưới đây, CodeWhisperer sẽ sinh ra nội dung hàm cho bạn.

**Đầu vào người dùng (JavaScript):**

```javascript
function standardDeviation(numbers)
```

**Kết quả:**

```javascript
function standardDeviation(numbers) {
  let mean = numbers.reduce((a, b) => a + b) / numbers.length;
  let variance =
    numbers.reduce((a, b) => a + Math.pow(b - mean, 2)) / numbers.length;
  return Math.sqrt(variance);
}
```

#### Tạo Hàm từ Chú Thích

Đôi khi, một chữ ký hàm tốt một mình không đủ để truyền đạt hành vi mong muốn của một hàm. Trong những trường hợp đó, bạn có thể sử dụng một chú thích mã lệnh chi tiết như một gợi ý cho CodeWhisperer. Tôi khuyên bạn nên sử dụng ký hiệu chú thích tài liệu của ngôn ngữ của bạn khi sử dụng kỹ thuật này.

**Đầu vào người dùng (JavaScript):**

```javascript
/**
 * Given a list that contains some numbers and strings, format them into a string
 * in which the numbers are prepended with "#" and the strings are wrapped in
 * double quotes.
 */
```

**Kết quả:**

```javascript
/**
 * Given a list that contains some numbers and strings, format them into a string
 * in which the numbers are prepended with "#" and the strings are wrapped in
 * double quotes.
 */
function formatList(list) {
  return list
    .map((item) => {
      if (typeof item === "number") {
        return `#${item}`;
      } else {
        return `"${item}"`;
      }
    })
    .join(", ");
}
```

Đó là cách bạn có thể sử dụng CodeWhisperer để tạo ra các hàm một cách tự động hoặc từ chú thích mô tả trong mã của mình.

---
#### Tạo các lớp

Bạn có thể tạo ra các lớp hoàn chỉnh hoặc một phần từ một comment duy nhất trong mã. Comment này nên mô tả các thuộc tính chính và hành vi của lớp. Thường chỉ cần những mô tả đơn giản.

Đầu vào người dùng (TypeScript):

```typescript
/**
 * Một thư mục có tên, các con, và một thư mục cha tùy chọn. Một con không thể được thêm
 * hai lần.
 */
```

Kết quả:

Sau khi viết đoạn comment trên, CodeWhisperer cung cấp nhiều gợi ý, bao gồm cài đặt sau đây, kèm theo comment tài liệu cho mỗi phương thức!

```typescript
/**
 * Một thư mục có tên, các con, và một thư mục cha tùy chọn. Một con không thể được thêm
 * hai lần.
 */
export class Folder {
  name: string;
  children: Folder[];
  parent?: Folder;

  constructor(name: string, parent?: Folder) {
    this.name = name;
    this.children = [];
    this.parent = parent;
  }

  /**
   * Thêm một con vào thư mục.
   * @param child Con cần thêm.
   * @returns True nếu con đã được thêm, false nếu con đã có trong danh sách.
   */
  addChild(child: Folder): boolean {
    if (this.children.includes(child)) {
      return false;
    }
    this.children.push(child);
    child.parent = this;
    return true;
  }

  /**
   * Xóa một con khỏi thư mục.
   * @param child Con cần xóa.
   * @returns True nếu con đã được xóa, false nếu không có trong danh sách.
   */
  removeChild(child: Folder): boolean {
    const index = this.children.indexOf(child);
    if (index === -1) {
      return false;
    }
    this.children.splice(index, 1);
    child.parent = undefined;
    return true;
  }
}
```

Bạn có thể thấy rằng, dựa trên đoạn comment, mã cài đặt được tạo ra, bao gồm cả các comment tài liệu cho mỗi phương thức.

---

#### Triển khai thuật toán với CodeWhisperer

CodeWhisperer cho phép bạn triển khai các thuật toán nổi tiếng một cách dễ dàng. Chỉ cần cho biết thuật toán nào bạn muốn áp dụng cho một vấn đề lập trình cụ thể, và nó sẽ thực hiện theo yêu cầu.

#### Đầu vào của người dùng (JavaScript):

```javascript
const actors = [ ... ];

// Sắp xếp các diễn viên theo tuổi bằng thuật toán merge sort.
```

#### Kết quả:

```javascript
const actors = [ ... ];

// Sắp xếp các diễn viên theo tuổi bằng thuật toán merge sort.
function mergeSort(arr) {
  if (arr.length < 2) {
    return arr;
  }

  const middle = Math.floor(arr.length / 2);
  const left = arr.slice(0, middle);
  const right = arr.slice(middle);

  return merge(mergeSort(left), mergeSort(right));
}

function merge(left, right) {
  const result = [];

  while (left.length && right.length) {
    if (left[0].age < right[0].age) {
      result.push(left.shift());
    } else {
      result.push(right.shift());
    }
  }

  while (left.length) {
    result.push(left.shift());
  }

  while (right.length) {
    result.push(right.shift());
  }

  return result;
}

console.log(mergeSort(actors));
```

Cảm ơn bạn đã sử dụng CodeWhisperer để triển khai thuật toán này!

---

#### Tăng cường viết các unit test

CodeWhisperer giúp tăng tốc quá trình triển khai các unit test. Không chỉ có khả năng triển khai logic cho hầu hết các unit test mà tôi yêu cầu, mà nó thường đề xuất các test cho các trường hợp biên mà tôi thậm chí chưa nghĩ đến.

Khi tôi muốn CodeWhisperer triển khai một unit test, tôi bắt đầu bằng việc khai báo điều kiện tôi đang kiểm tra và kết quả dự kiến như trong ví dụ sau.

```javascript
describe("Folder.addChild()", () => {
  it("when adding an existing folder should not add duplicate", () => {
    const folder = new Folder("root");
    const child = new Folder("child");
    folder.addChild(child);
    folder.addChild(child);
    expect(folder.children.length).toBe(1);
  });
});
```

Sau khi bạn đã viết một hoặc hai test, CodeWhisperer có khả năng đề xuất thêm các test mà không cần yêu cầu cụ thể.

**Mẹo:** Bạn sẽ nhận thấy rằng mô tả test của tôi bao gồm 1) hàm tôi đang kiểm tra, 2) điều kiện tôi đang kiểm tra, và 3) kết quả tôi mong đợi. Tuân theo mẫu ba phần này là một cách tuyệt vời để đảm bảo CodeWhisperer có ngữ cảnh cần thiết để triển khai logic test chất lượng cao.

---

#### Tạo dữ liệu mẫu với Code Whisper

Một trong những phát hiện thú vị mà tôi đã trải qua là Code Whisperer có thể tạo ra dữ liệu giả - hoặc thực sự là bất kỳ mã nào có mẫu lặp lại. Ví dụ, cho danh sách dưới đây, tôi chỉ nhập đối tượng "user" đầu tiên làm ví dụ, và Code Whisperer đã tiếp tục mẫu một cách hữu ích.

#### Nhập người dùng (JavaScript):

```javascript
const fakeUsers = [
  { name: "User 1", id: "user1" },
JavaScript
```

#### Kết quả:

```javascript
const fakeUsers = [
  { name: "User 1", id: "user1" },
  { name: "User 2", id: "user2" },
  { name: "User 3", id: "user3" },  
  { name: "User 4", id: "user4" },
  { name: "User 5", id: "user5" },
  { name: "User 6", id: "user6" }
]
JavaScript
```

Nó còn hoạt động để tạo ra các giá trị ngẫu nhiên nhưng có thể tin được như các tên được thấy dưới đây.

#### Nhập người dùng (JavaScript):

```javascript
const fakeUsers = [
  { name: "Sally", id: "user1" },
JavaScript
```

#### Kết quả:

```javascript
const fakeUsers = [
  { name: "Sally", id: "user1" },
  { name: "Bob", id: "user2" },
  { name: "Joe", id: "user3" },
  { name: "Jane", id: "user4" },
  { name: "Jill", id: "user5" },
  { name: "Jack", id: "user6" }
]
```

---