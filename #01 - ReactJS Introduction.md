## ReactJS Introduction

### ReactJS là gì?

ReactJS là một thư viện JavaScript mã nguồn mở được sử dụng để xây dựng giao diện người dùng (UI) cho các ứng dụng web. Nó được phát triển bởi Facebook và hiện được sử dụng rộng rãi trong ngành công nghệ.

#### Server-side rendering và Client-side rendering?

- Server-side rendering (SSR) là quá trình tạo và hiển thị trang web trên máy chủ trước khi gửi đến trình duyệt của người dùng. Kỹ thuật SSR giúp cải thiện thời gian tải trang ban đầu và cải thiện trải nghiệm người dùng.
    
- Client-side rendering (CSR) là quá trình tạo và hiển thị trang web trên trình duyệt của người dùng bằng cách sử dụng JavaScript. Kỹ thuật CSR cho phép tương tác trực tiếp với trang web mà không cần tải lại trang.
    

#### Single-page application và Multi-page application?

- Single-page application (SPA) là một ứng dụng web tương tác mà không cần tải lại trang. Thay vì tải lại toàn bộ trang web, SPA chỉ tải các phần tử cần thiết và thay đổi nội dung một cách động.
    
- Multi-page application (MPA) là một ứng dụng web có nhiều trang riêng biệt. Khi người dùng chuyển đổi giữa các trang, trình duyệt sẽ tải lại toàn bộ trang mới.
    

### Cách React hoạt động?

### Rendering Elements (Hiển thị các phần tử)

React hoạt động bằng cách xây dựng và cập nhật DOM (Document Object Model) dựa trên các phần tử (elements). Mỗi phần tử trong React là một đại diện cho một phần tử UI cụ thể. Khi các phần tử thay đổi, React sẽ cập nhật DOM để phản ánh các thay đổi đó.

Để hiển thị một thành phần React, chúng ta sử dụng hàm ReactDOM.render(). Hàm này nhận vào một phần tử React và một nút gốc trong DOM để gắn kết phần tử React đó.

Ví dụ:

``` jsx
import React from 'react';
import ReactDOM from 'react-dom';

const element = <h1>Hello, React!</h1>;

ReactDOM.render(element, document.getElementById('root'));
```
Trong ví dụ trên, chúng ta đã tạo một phần tử React <h1>Hello, React!</h1> và gắn kết nó vào nút có id là root trong DOM.

#### Virtual DOM (DOM ảo)

Virtual DOM là một bản sao của DOM thực sự được React sử dụng để tính toán các thay đổi cần được áp dụng cho DOM. Thay vì thực hiện các thay đổi trực tiếp trên DOM thật, React so sánh Virtual DOM với DOM trước và sau khi thay đổi để xác định các thay đổi cần được áp dụng. Việc sử dụng Virtual DOM giúp tăng hiệu suất và tối ưu quá trình render.

### JSX là gì?

JSX (JavaScript XML) là một phần mở rộng cú pháp của JavaScript cho phép viết mã HTML tương tự như cú pháp XML trong mã JavaScript. JSX giúp kết hợp mã JavaScript và mã HTML trong cùng một file, giúp việc tạo và quản lý các component dễ dàng hơn.

Ví dụ về viết JSX:

```jsx
import React from 'react';

const element = <h1>Hello, JSX!</h1>;
Trong ví dụ trên, chúng ta đã sử dụng JSX để tạo một phần tử React <h1>Hello, JSX!</h1>. JSX sẽ được biên dịch thành mã JavaScript thông qua Babel để sử dụng trong ứng dụng React.
```
### Cấu trúc thư mục

- **Thư mục Assets:** Thư mục này chứa các tệp hình ảnh và tệp CSS để sử dụng trong dự án. Chúng ta có thể lưu trữ các kiểu CSS toàn cục ở đây.
    
- **Thư mục Layouts:** Thư mục này chứa các layout (bố cục) có sẵn cho toàn bộ dự án, chẳng hạn như header (đầu trang), footer (cuối trang), vv. Chúng ta có thể lưu trữ mã của header, footer hoặc thanh bên ở đây và sau đó gọi chúng khi cần.
    
- **Thư mục Components:** Thư mục này chứa một tập hợp các component UI như nút (button), hộp thoại (modal), đầu vào (input), v.v., có thể được sử dụng trong nhiều tệp trong dự án.
    
- **Thư mục Pages:** Các tệp trong thư mục pages xác định các đường dẫn (routes) của ứng dụng React. Thông thường, chúng được nhóm các component lại với nhau.
    
- **Thư mục Middleware:** Thư mục này chứa các middleware cho phép xử lý các hiệu ứng phụ (side effects) trong ứng dụng. Nó được sử dụng khi chúng ta sử dụng Redux với React.
    
- **Thư mục Routes:** Thư mục này chứa tất cả các đường dẫn (routes) của ứng dụng.
    
- **Thư mục Config:** Thư mục này chứa một tệp cấu hình, nơi chúng ta lưu trữ các biến môi trường trong config.js.
    
- **Thư mục Services:** Thư mục này sẽ được thêm nếu chúng ta sử dụng Redux trong dự án. Bên trong nó, có 3 thư mục con là actions, reducers và constants để quản lý trạng thái.
    
- **Thư mục Utils:** Thư mục này chứa một số hàm được sử dụng lặp lại thường xuyên trong dự án.
    

## Cài đặt một ứng dụng React

### Tạo ứng dụng React với Webpack và Babel

Để tạo một ứng dụng React với Webpack và Babel, bạn có thể thực hiện các bước sau:

1. Tạo thư mục cho dự án của bạn và di chuyển vào thư mục đó.
    
2. Mở Terminal và chạy lệnh sau để khởi tạo một dự án npm mới:
    

```shell
npm init -y
```


3. Tiếp theo, cài đặt các gói cần thiết:

``` shell
npm install react react-dom webpack webpack-cli babel-loader @babel/core @babel/preset-react --save-dev
```

4. Tạo một tệp webpack.config.js trong thư mục gốc của dự án và cấu hình nó như sau:

``` javascript
const path = require('path');
module.exports = {
	entry: './src/index.js',
	output: {
		filename: 'bundle.js',
		path: path.resolve(__dirname, 'dist'),
	},   
	module: {     
		rules: [       
			{         
				test: /\.js$/,         
				exclude: /node_modules/,         
				use: {           
					loader: 'babel-loader',           
					options: {             
						presets: ['@babel/preset-react'],           
					},         
				},       
			},     
		],   
	}, 
};
```

5. Tạo một thư mục `src` trong thư mục gốc của dự án và tạo tệp `index.js` trong đó.
    
6. Trong tệp `index.js`, nhập React và ReactDOM và viết mã JSX của bạn.
    
7. Mở tệp `package.json` và thêm một script để chạy webpack:
    

``` json
"scripts": {   
	"build": "webpack --mode production" 
}
```

8. Chạy lệnh sau để biên dịch ứng dụng React của bạn:


``` shell
npm run build
```

9. Khi quá trình biên dịch hoàn tất, ứng dụng của bạn sẽ được biên dịch vào thư mục `dist` và bạn có thể mở tệp HTML trong trình duyệt để xem ứng dụng.

### Create-React-App

Create React App là một công cụ mạnh mẽ để nhanh chóng khởi tạo một dự án React với cấu hình mặc định đã được thiết lập.

Để tạo một ứng dụng React bằng Create React App, bạn có thể thực hiện các bước sau:

1. Mở Terminal và chạy lệnh sau để cài đặt Create React App (nếu chưa có):

``` bash
npm install -g create-react-app
```

2. Tạo một dự án mới bằng cách chạy lệnh sau:

``` shell
npx create-react-app my-app
```

3. Di chuyển vào thư mục dự án mới:

bashCopy code

``` shell
cd my-app
```

4. Chạy ứng dụng của bạn bằng cách chạy lệnh:

``` shell
npm start
```

Ứng dụng React của bạn sẽ được chạy trên `http://localhost:3000` và bạn sẽ thấy trang chào mừng mặc định của Create React App hiển thị trên trình duyệt của bạn.

## Các chủ đề cơ bản

### Component là gì?

Trong React, một component là một đơn vị độc lập có thể tái sử dụng của giao diện người dùng (UI). Nó chứa các phần tử UI, các logic xử lý và có thể nhận đầu vào từ các props.

### Functional Component (Component hàm)

Functional Component là một cách khai báo component trong React bằng cách sử dụng hàm. Đây là một phong cách viết component đơn giản và ngắn gọn.

Ví dụ về Functional Component:


``` jsx
import React from 'react';

const MyComponent = () => {   
	return <h1>Hello, World!</h1>; 
};  

export default MyComponent;
```

Trong ví dụ trên, chúng ta đã tạo một Functional Component đơn giản trả về một thẻ `<h1>` hiển thị nội dung "Hello, World!".

### Cách sử dụng CSS và JS trong component?

Để sử dụng CSS trong một component, chúng ta có thể sử dụng các phương pháp như Inline CSS, CSS Modules, hoặc thư viện CSS-in-JS như styled-components. Bạn có thể áp dụng các lớp CSS trực tiếp vào các phần tử hoặc sử dụng các phương pháp tương tự để quản lý CSS cho component.

Để sử dụng JavaScript trong một component, chúng ta có thể viết mã JavaScript bên trong hàm render của component hoặc tạo các phương thức và xử lý sự kiện trong component.

### Props

Props (viết tắt của "properties") là một cách để truyền dữ liệu từ component cha đến component con trong React. Props là các đối tượng không thể thay đổi (immutable) và được truyền từ component cha dưới dạng thuộc tính. Component con có thể sử dụng props để hiển thị dữ liệu hoặc điều khiển hành vi của mình.

Ví dụ về sử dụng Props:

``` jsx
import React from 'react';

const Greeting = (props) => {
	return <h1>Hello, {props.name}!</h1>; 
};  

export default Greeting;
```

Trong ví dụ trên, component Greeting nhận một prop là `name` và hiển thị nội dung "Hello, {props.name}!". Khi sử dụng component này, chúng ta có thể truyền giá trị cho `name` như sau:

```jsx
import React from 'react'; 
import Greeting from './Greeting';  
const App = () => {
	return <Greeting name="John" />; 
};  
export default App;
```

Ứng dụng sẽ hiển thị "Hello, John!"
