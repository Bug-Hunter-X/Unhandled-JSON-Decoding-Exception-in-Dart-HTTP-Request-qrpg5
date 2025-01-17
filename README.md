# Unhandled JSON Decoding Exception in Dart HTTP Request

This repository demonstrates a common error in Dart when handling HTTP requests and JSON decoding: failure to specifically handle `FormatException` thrown by `jsonDecode`. The `bug.dart` file shows the flawed code, while `bugSolution.dart` presents a more robust solution.

The issue arises when the API response is not valid JSON, causing `jsonDecode` to throw a `FormatException`. The original code catches general exceptions, making it harder to identify the specific problem.  The solution improves error handling by using a `try-catch` block specifically to handle `FormatException`, providing more informative error messages and more robust error handling.