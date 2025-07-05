Первая программа
```c++
// myfirst.cpp

#include <iostream>  // директива препроцессора

int main() {
  using namespace std;

  cout << "Come up and C++ me some time.";
  cout << endl;
  cout << "You won't regret it!" << endl;

  return 0;
}
```

Скомпилировать удалось такой командой
```bash
$ clang++ -std=gnu++14 -stdlib=libc++ -fcolor-diagnostics -g gurobi.cpp -o gurobi
```
NB! Здесь нужно использовать именно `clang++`, а не `clang`! Компиляция с `clang` выдает такую ошибку
```bash
Undefined symbols for architecture arm64:
  "std::__1::locale::use_facet(std::__1::locale::id&) const", referenced from:
      std::__1::ctype<char> const& std::__1::use_facet[abi:ne190102]<std::__1::ctype<char>>(std::__1::locale const&) in gurobi-8e4f3d.o
  "std::__1::ios_base::getloc() const", referenced from:
      std::__1::basic_ios<char, std::__1::char_traits<char>>::widen[abi:ne190102](char) const in gurobi-8e4f3d.o
  "std::__1::basic_string<char, std::__1::char_traits<char>, std::__1::allocator<char>>::__init(unsigned long, char)", referenced from:
      std::__1::basic_string<char, std::__1::char_traits<char>, std::__1::allocator<char>>::basic_string[abi:ne190102](unsigned long, char) in gurobi-8e4f3d.o
  "std::__1::basic_string<char, std::__1::char_traits<char>, std::__1::allocator<char>>::~basic_string()", referenced from:
      std::__1::ostreambuf_iterator<char, std::__1::char_traits<char>> std::__1::__pad_and_output[abi:ne190102]<char, std::__1::char_traits<char>>(std::__1::ostreambuf_iterator<char, std::__1::char_traits<char>>, char const*, char const*, char const*, std::__1::ios_base&, char) in gurobi-8e4f3d.o
      std::__1::ostreambuf_iterator<char, std::__1::char_traits<char>> std::__1::__pad_and_output[abi:ne190102]<char, std::__1::char_traits<char>>(std::__1::ostreambuf_iterator<char, std::__1::char_traits<char>>, char const*, char const*, char const*, std::__1::ios_base&, char) in gurobi-8e4f3d.o
  "std::__1::basic_ostream<char, std::__1::char_traits<char>>::put(char)", referenced from:
      std::__1::basic_ostream<char, std::__1::char_traits<char>>& std::__1::endl[abi:ne190102]<char, std::__1::char_traits<char>>(std::__1::basic_ostream<char, std::__1::char_traits<char>>&) in gurobi-8e4f3d.o
  "std::__1::basic_ostream<char, std::__1::char_traits<char>>::flush()", referenced from:
      std::__1::basic_ostream<char, std::__1::char_traits<char>>& std::__1::endl[abi:ne190102]<char, std::__1::char_traits<char>>(std::__1::basic_ostream<char, std::__1::char_traits<char>>&) in gurobi-8e4f3d.o
  "std::__1::basic_ostream<char, std::__1::char_traits<char>>::sentry::sentry(std::__1::basic_ostream<char, std::__1::char_traits<char>>&)", referenced from:
      std::__1::basic_ostream<char, std::__1::char_traits<char>>& std::__1::__put_character_sequence[abi:ne190102]<char, std::__1::char_traits<char>>(std::__1::basic_ostream<char, std::__1::char_traits<char>>&, char const*, unsigned long) in gurobi-8e4f3d.o
  "std::__1::basic_ostream<char, std::__1::char_traits<char>>::sentry::~sentry()", referenced from:
      std::__1::basic_ostream<char, std::__1::char_traits<char>>& std::__1::__put_character_sequence[abi:ne190102]<char, std::__1::char_traits<char>>(std::__1::basic_ostream<char, std::__1::char_traits<char>>&, char const*, unsigned long) in gurobi-8e4f3d.o
      std::__1::basic_ostream<char, std::__1::char_traits<char>>& std::__1::__put_character_sequence[abi:ne190102]<char, std::__1::char_traits<char>>(std::__1::basic_ostream<char, std::__1::char_traits<char>>&, char const*, unsigned long) in gurobi-8e4f3d.o
	  ...
```
