# Reflection
## Experiment 2.1
![Experiment 2.1](docs/img/Experiment_2_1.png)
### How to run Server:
- **Jalankan server** (dari direktori `chat-async`):
```bash
cargo run --bin server
```
Server akan mulai dan mendengarkan pada port `2000`.
- **Jalankan client** (di terminal terpisah, ulangi untuk beberapa client):
```bash
cargo run --bin client
```
Setiap client dapat mengirim pesan.

### What happened when client sent message
1. Client mengirim pesan ke server melalui koneksi WebSocket ketika client menekan Enter.
2. Server menerima pesan dan mencatat log, misalnya: `From client 127.0.0.1:59069 "Client-1"`.
3. Server meneruskan pesan tersebut ke semua client yang terhubung menggunakan channel broadcast (mis. `tokio::sync::broadcast`).
4. Semua client yang terhubung menerima broadcast dan menampilkan pesan dari server, misalnya: `From server: Client-2`.

## Experiment 2.2
![Experiment 2.2](docs/img/Experiment_2_2.png)


## Experiment 2.3
![Experiment 2.3](docs/img/Experiment_2_3.png)