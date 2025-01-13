
# 🚀 Multithreaded Rust Server for Embedded Systems Task

This repository contains a multithreaded server implemented in Rust, demonstrating efficient client-server communication using Protocol Buffers. The project features a server, client, and test suite for handling concurrent connections.

---

## 📂 Project Structure

```plaintext
.
├── Cargo.toml            # Rust dependencies and configuration
├── build.rs              # Build script for generating Protobuf code
├── proto/                # Protocol Buffers definitions
│   └── messages.proto
├── src/
│   ├── main.rs           # Main entry point for the server
│   ├── lib.rs            # Exposes server, client, and message modules
│   ├── server.rs         # Server implementation
│   ├── client.rs         # Client implementation
│   └── messages.rs       # Generated Protobuf code
└── tests/
    └── client_test.rs    # Test suite for server functionality
```

---

## 🛠️ Prerequisites

Before running the project, ensure you have the following installed:

- **Rust**: Latest stable version from [rustup.rs](https://rustup.rs/).
- **Cargo**: Rust's package manager (included with Rust).
- **Protocol Buffers**: Install the `protoc` compiler as per the [official guide](https://grpc.io/docs/protoc-installation/).

---

## 🚀 Getting Started

### 1. Clone the Repository

Clone the repository to your local machine using the following command:

```bash
git clone https://github.com/Mahmoudali98/Embedded-recruitment-task-0.0.1.git
cd Embedded-recruitment-task-0.0.1
```

---

### 2. Build the Project

To compile the project, run the following command:

```bash
cargo build
```

---

### 3. Run the Server

To start the server, use:

```bash
cargo run
```

The server will start listening on `localhost:8080`, and you'll see logs like:

```plaintext
[INFO] Server is running on localhost:8080
```

---

### 4. Run the Test Suite

To verify the server functionality, run:

```bash
cargo test -- --nocapture
```

The `--nocapture` flag ensures that test logs are displayed in the terminal. Sample output:

```plaintext
running 1 test
[INFO] Starting test_client_echo_message...
[INFO] Server stopped.
test test_client_echo_message ... ok

test result: ok. 1 passed; 0 failed; 0 ignored
```

---

### 5. Connect a Client

Use the client code in `client.rs` to connect to the server and send messages. Feel free to modify the client implementation as needed.

---

## 🧩 Key Features

- **Multithreaded Server**: Leverages a thread pool for handling multiple client connections efficiently.
- **Protocol Buffers**: Uses Protobuf for encoding/decoding messages.
- **Comprehensive Test Suite**: Verifies the functionality of the client-server interaction.
- **Logging**: Provides structured logging using `log` and `env_logger` crates.

---

## 📦 Dependencies

The project utilizes the following Rust crates:

- `log`: Logging for application events.
- `env_logger`: Initializes environment-based logging.
- `prost`: Encodes and decodes Protocol Buffer messages.
- `threadpool`: Manages a pool of threads for concurrent client connections.
- `prost-build`: Generates Rust code from Protocol Buffer definitions.

---

## 📚 Additional Learning Resources

For those new to Rust, these resources may be helpful:

- [Rust Programming Playlist](https://www.youtube.com/playlist?list=PL5dTjWUk_cPYOPWpUwmOLatvUB9ZwHH7p)
- [The Rust Programming Language Book](https://doc.rust-lang.org/book/)
- [Rust by Example](https://doc.rust-lang.org/rust-by-example/)

---

## 📝 Important Notes

- The server supports multiple concurrent clients using a thread pool architecture.
- The test suite includes a basic `test_client_echo_message` test to verify message echoing.
- You can expand the server and client to handle additional message types or functionality.

---

## 🙌 Contributing

Contributions are welcome! To contribute:

1. Fork the repository.
2. Create a new feature branch:
   ```bash
   git checkout -b feature/YourFeatureName
   ```
3. Commit your changes:
   ```bash
   git commit -m 'Add some feature'
   ```
4. Push your branch:
   ```bash
   git push origin feature/YourFeatureName
   ```
5. Submit a pull request.

---

## 🛡️ Optional: Add Badges

To enhance your README with status indicators, consider adding badges like:

```markdown
![Rust](https://img.shields.io/badge/Rust-v1.60+-orange)
```
