## To Read
- [Iterators](https://en.cppreference.com/w/cpp/iterator) -> [spans](https://en.cppreference.com/w/cpp/container/span) -> [ranges](https://en.cppreference.com/w/cpp/ranges)
- [constexpr](https://en.cppreference.com/w/cpp/language/constexpr)
	- Can be evaluated at compile-time instead of runtime
	- Shift processing to compile-time, quicker at runtime
	- Can be run at run-time
	- Not the only way to be used in constant expressions
		- `const`
	- Can use with const
		- `constexpr const int N = 5;`
			- same as `constexpr int N = 5;`
		- `constexpr` implies `const`


## Conan
cmake-conan
[https://github.com/conan-io/cmake-conan](https://github.com/conan-io/cmake-conan)

[https://cliutils.gitlab.io/modern-cmake/](https://cliutils.gitlab.io/modern-cmake/)
