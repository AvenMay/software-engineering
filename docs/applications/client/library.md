# Libaray

### 🌐 各语言主流 HTTP Client 推荐表

| **编程语言**             | **标准库 / 内置 (Built-in)**          | **主流第三方库 (Third-party)**                               | **特点与适用场景建议**                                       |
| ------------------------ | ------------------------------------- | ------------------------------------------------------------ | ------------------------------------------------------------ |
| **Python**               | `urllib.request`                      | **requests** **httpx** **aiohttp**                           | **requests**: 事实标准，极其人性化，适合绝大多数同步请求。 **httpx**: 新生代力量，API 类似 requests，但**原生支持异步** (asyncio) 和 HTTP/2。 **aiohttp**: 专为异步高并发设计的库。 |
| **Java**                 | `java.net.http.HttpClient` (Java 11+) | **OkHttp** **Apache HttpClient** **Retrofit** **WebClient** (Spring) | **Java 11 HttpClient**: 现代内置首选，支持响应式和 HTTP/2。 **OkHttp**: 性能极佳，Android 和后端通用。 **Apache HttpClient**: 历史悠久，功能繁多，适合极其复杂的企业级需求。 **Retrofit**: 面向接口的类型安全 HTTP 客户端（底层基于 OkHttp）。 |
| **JavaScript / Node.js** | `Fetch API` (浏览器 & Node 18+)       | **Axios** **Got** (Node) **node-fetch**                      | **Fetch**: 现代原生标准，能用内置就用内置。 **Axios**: 浏览器和 Node.js 通用，支持拦截器、自动 JSON 转换，最受欢迎。 **Got**: 专门针对 Node.js 优化的强大底层网络库。 |
| **Go (Golang)**          | `net/http`                            | **go-resty/resty** **imroc/req**                             | **net/http**: Go 的标准库极其强大，超过 80% 的情况直接用它就够了。 **Resty**: 提供了方便的链式调用、自动重试和 JSON 绑定，适合重度 RESTful 交互。 |
| **C# / .NET**            | `System.Net.Http.HttpClient`          | **RestSharp** **Flurl.Http**                                 | **HttpClient**: .NET 的绝对核心，现代 C# 开发通常直接使用它并通过 `IHttpClientFactory` 管理。 **Flurl**: 流畅的链式 API，URL 拼接极其优雅，非常易于单元测试。 |
| **Rust**                 | 无 (标准库不包含高级 HTTP 功能)       | **reqwest** **hyper**                                        | **reqwest**: Rust 生态中最高频使用的 HTTP 客户端，基于 hyper 封装，支持异步和阻塞 API。 **hyper**: 底层、超高性能 HTTP 库，通常用于构建框架或其他库。 |
| **C++**                  | 无                                    | **libcurl** **CPR** **cpp-httplib**                          | **libcurl**: C 语言库，是跨平台 HTTP 调用的工业标准，但原生 API 较繁琐。 **CPR**: (C++ Requests) 受 Python requests 启发，对 libcurl 进行了非常优雅的面向对象封装。 **cpp-httplib**: 单头文件库，极简易用，无需复杂编译配置。 |
| **PHP**                  | `cURL` 扩展 `file_get_contents`       | **Guzzle** **Symfony HttpClient**                            | **Guzzle**: PHP 届绝对的事实标准，功能全面，支持中间件和异步请求。 **Symfony HttpClient**: Symfony 组件，轻量、低耦合且性能优异。 |
| **Swift / iOS**          | `URLSession`                          | **Alamofire**                                                | **URLSession**: Apple 官方提供，已完全支持 `async/await`，能满足绝大多数需求。 **Alamofire**: iOS 开发中最著名的网络库，提供极其优雅的链式封装、认证和网络状态监听。 |
| **Kotlin / Android**     | 同 Java                               | **Ktor Client** **OkHttp** / **Retrofit**                    | **Ktor Client**: Kotlin 官方出品，完美契合协程 (Coroutines)，且支持跨平台 (KMP)。 注：Android 开发中依然大量使用 Retrofit/OkHttp 的组合。 |
| **Ruby**                 | `Net::HTTP`                           | **Faraday** **HTTParty** **RestClient**                      | **Faraday**: 提供统一接口并支持切换底层适配器 (Adapter)，中间件架构非常灵活。 **HTTParty**: 使用简单，通过 `include HTTParty` 即可让任何类具备发请求的能力。 |

### 💡 核心选型建议

1. **追求极简和少依赖**：优先查看该语言的**内置标准库**。近年来，许多语言（如 Java 11、Node.js 18+、现代 Swift 等）都对内置的 HTTP Client 进行了大幅重构，原生已经支持 `async/await` 或 Promise，能够直接替代大部分基础第三方库。
2. **构建重度微服务/REST 交互**：选择具备**拦截器 (Interceptors)**、**自动重试 (Retries)** 和 **JSON 自动序列化**的第三方库（例如 Python 的 `httpx`、Java 的 `Retrofit`、JS 的 `Axios`、PHP 的 `Guzzle`）。
3. **高并发数据抓取 (Scraping)**：优先选择底层采用异步非阻塞架构的库（例如 Python 的 `aiohttp`，Rust 的 `reqwest`，Node 的 `Got`）。