# Context

React Context menyediakan cara untuk oper data melalui diagram komponen tanpa harus oper props secara manual di setiap tingkat.

Salah satu alasan untuk menggunakan React Context dikarenakan datanya tidak digunakan pada component lain

## Kapan harus menggunakan context?

Context dirancang untuk berbagi data yang dapat dianggap “global” untuk diagram komponen React, seperti pengguna terotentikasi saat ini, tema, atau bahasa yang disukai. Misalnya, dalam kode di bawah ini kita secara manual memasang prop “theme” untuk memberi style pada komponen Button:

```class App extends React.Component {
  render() {
    return <Toolbar theme="dark" />;
  }
}

function Toolbar(props) {
  // The Toolbar component must take an extra "theme" prop
  // and pass it to the ThemedButton. This can become painful
  // if every single button in the app needs to know the theme
  // because it would have to be passed through all components.
  return (
    <div>
      <ThemedButton theme={props.theme} />
    </div>
  );
}

class ThemedButton extends React.Component {
  render() {
    return <Button theme={this.props.theme} />;
  }
}
```

<br>

# React Testing

React Testing Library adalah seperangkat helpers yang memungkinkan Anda mengetes komponen pada React tanpa bergantung pada detail implementasinya. Pendekatan ini membuat refactoring menjadi mudah dan juga mendorong kita untuk menerapkan best practices untuk aksesbilitas.

React Testing Librarydibangun di atas DOM Testing Librarydengan menambahkan API untuk bekerja dengan komponen React.

Secara garis besar testing terbagi menjadi 2 yaitu Manual Testing dan Automated Testing

Dengan memberikan keuntungan untuk software engineer menjadi salah satu alasan mengapa Testing dalam Software Development itu sangat penting

Regression merupakan tipe testing yang dilakukan untuk mengecek apakah suatu fitur baru yang ditambahkan ke dalam aplikasi akan membuat error atau bug pada fitur sebelumnya