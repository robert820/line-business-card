# Third-Party Notices / 第三方元件授權聲明

This software includes the third-party components below. They are licensed under their own terms, which are available in each project's repository or package page. The proprietary freeware [LICENSE](LICENSE) of this project does not apply to them. The components are listed from the project's lock files (`Cargo.lock`, `package-lock.json`), production dependencies only.

本軟體包含下列第三方元件，各元件依其原授權條款提供，授權全文可於各專案儲存庫或套件頁面查閱。本專案之 [LICENSE](LICENSE) 專有免費軟體授權不適用於這些元件。清單依專案鎖定檔（`Cargo.lock`、`package-lock.json`）產生，僅列正式執行所需之相依套件。

---

## 1. LINE Front-end Framework (LIFF) — LY Corporation

- Packages / 套件：`@line/liff` and its `@liff/*` sub-packages (51 packages, version 2.32.0) / `@line/liff` 及其 `@liff/*` 子套件（共 51 個，版本 2.32.0）
- License / 授權：Proprietary. Provided by LY Corporation; use is governed by the LINE Developers Agreement (package license field: "SEE LICENSE IN README.md"). / 專有授權，由 LY Corporation 提供，使用須遵守 LINE Developers Agreement（套件授權欄位為「SEE LICENSE IN README.md」）。
- Source / 來源：https://www.npmjs.com/package/@line/liff
- Used only by the optional LINE integration. / 僅用於選用的 LINE 整合功能。

---

## 2. Rust crates

License expressions are taken from each crate's `Cargo.toml`. Where a crate offers a choice (e.g. `MIT OR Apache-2.0`), you may use it under either license. / 授權標示取自各套件 `Cargo.toml`；若為多重授權（如 `MIT OR Apache-2.0`），可擇一適用。

| Crate | Version | License |
|---|---|---|
| adler2 | 2.0.1 | 0BSD OR MIT OR Apache-2.0 |
| allocator-api2 | 0.2.21 | MIT OR Apache-2.0 |
| anyhow | 1.0.104 | MIT OR Apache-2.0 |
| argon2 | 0.5.3 | MIT OR Apache-2.0 |
| atoi | 2.0.0 | MIT (*) |
| atomic-waker | 1.1.2 | Apache-2.0 OR MIT |
| axum | 0.8.9 | MIT |
| axum-core | 0.5.6 | MIT |
| base64 | 0.22.1 | MIT OR Apache-2.0 |
| base64ct | 1.8.3 | Apache-2.0 OR MIT |
| bitflags | 2.13.2 | MIT OR Apache-2.0 |
| blake2 | 0.10.6 | MIT OR Apache-2.0 |
| block-buffer | 0.10.4 | MIT OR Apache-2.0 |
| bytemuck | 1.25.2 | Zlib OR Apache-2.0 OR MIT |
| byteorder-lite | 0.1.0 | Unlicense OR MIT |
| bytes | 1.12.1 | MIT |
| cfg-if | 1.0.5 | MIT OR Apache-2.0 |
| chrono | 0.4.45 | MIT OR Apache-2.0 |
| core_detect | 1.0.0 | MIT/Apache-2.0 |
| cpufeatures | 0.2.17 | MIT OR Apache-2.0 |
| crc | 3.4.0 | MIT OR Apache-2.0 (*) |
| crc-catalog | 2.5.0 | MIT OR Apache-2.0 |
| crc32fast | 1.5.5 | MIT OR Apache-2.0 (*) |
| crossbeam-queue | 0.3.14 | MIT OR Apache-2.0 (*) |
| crossbeam-utils | 0.8.23 | MIT OR Apache-2.0 |
| crypto-common | 0.1.7 | MIT OR Apache-2.0 |
| digest | 0.10.7 | MIT OR Apache-2.0 (*) |
| displaydoc | 0.2.7 | MIT OR Apache-2.0 (*) |
| dotenvy | 0.15.7 | MIT |
| either | 1.19.0 | MIT OR Apache-2.0 (*) |
| encoding_rs | 0.8.44 | (Apache-2.0 OR MIT) AND BSD-3-Clause |
| equivalent | 1.0.3 | Apache-2.0 OR MIT |
| event-listener | 5.4.2 | Apache-2.0 OR MIT (*) |
| fdeflate | 0.3.7 | MIT OR Apache-2.0 |
| flate2 | 1.1.11 | MIT OR Apache-2.0 |
| flume | 0.11.1 | Apache-2.0/MIT (*) |
| foldhash | 0.1.5 | Zlib |
| form_urlencoded | 1.2.2 | MIT OR Apache-2.0 (*) |
| futures-channel | 0.3.34 | MIT OR Apache-2.0 (*) |
| futures-core | 0.3.34 | MIT OR Apache-2.0 |
| futures-executor | 0.3.34 | MIT OR Apache-2.0 (*) |
| futures-intrusive | 0.5.0 | MIT OR Apache-2.0 (*) |
| futures-io | 0.3.34 | MIT OR Apache-2.0 |
| futures-sink | 0.3.34 | MIT OR Apache-2.0 |
| futures-task | 0.3.34 | MIT OR Apache-2.0 |
| futures-util | 0.3.34 | MIT OR Apache-2.0 (*) |
| generic-array | 0.14.7 | MIT (*) |
| getrandom | 0.2.17 | MIT OR Apache-2.0 |
| getrandom | 0.4.3 | MIT OR Apache-2.0 |
| hashbrown | 0.15.5 | MIT OR Apache-2.0 (*) |
| hashbrown | 0.17.1 | MIT OR Apache-2.0 |
| hashlink | 0.10.0 | MIT OR Apache-2.0 (*) |
| heck | 0.5.0 | MIT OR Apache-2.0 |
| hex | 0.4.3 | MIT OR Apache-2.0 |
| html-escape | 0.2.15 | MIT |
| http | 1.5.0 | MIT OR Apache-2.0 (*) |
| http-body | 1.1.0 | MIT (*) |
| http-body-util | 0.1.5 | MIT (*) |
| http-range-header | 0.4.2 | MIT |
| httparse | 1.10.1 | MIT OR Apache-2.0 |
| httpdate | 1.0.3 | MIT OR Apache-2.0 |
| hyper | 1.12.0 | MIT (*) |
| hyper-util | 0.1.21 | MIT |
| icu_collections | 2.4.0 | Unicode-3.0 (*) |
| icu_locale_core | 2.4.0 | Unicode-3.0 (*) |
| icu_normalizer | 2.4.0 | Unicode-3.0 |
| icu_normalizer_data | 2.4.0 | Unicode-3.0 |
| icu_properties | 2.4.0 | Unicode-3.0 |
| icu_properties_data | 2.4.0 | Unicode-3.0 |
| icu_provider | 2.4.0 | Unicode-3.0 (*) |
| idna | 1.1.0 | MIT OR Apache-2.0 |
| idna_adapter | 1.2.2 | Apache-2.0 OR MIT |
| image | 0.25.10 | MIT OR Apache-2.0 |
| image-webp | 0.2.4 | MIT OR Apache-2.0 |
| indexmap | 2.14.2 | Apache-2.0 OR MIT (*) |
| itoa | 1.0.19 | MIT OR Apache-2.0 |
| lazy_static | 1.5.1 | MIT OR Apache-2.0 |
| libsqlite3-sys | 0.30.1 | MIT |
| litemap | 0.8.3 | Unicode-3.0 |
| lock_api | 0.4.14 | MIT OR Apache-2.0 (*) |
| log | 0.4.35 | MIT OR Apache-2.0 |
| matchers | 0.2.0 | MIT |
| matchit | 0.8.4 | MIT AND BSD-3-Clause |
| memchr | 2.8.3 | Unlicense OR MIT |
| mime | 0.3.18 | MIT OR Apache-2.0 |
| mime_guess | 2.0.5 | MIT |
| miniz_oxide | 0.8.9 | MIT OR Zlib OR Apache-2.0 |
| miniz_oxide | 0.9.1 | MIT OR Zlib OR Apache-2.0 |
| mio | 1.2.4 | MIT (*) |
| moxcms | 0.8.1 | BSD-3-Clause OR Apache-2.0 |
| multer | 3.1.0 | MIT |
| multiversion_no_op | 1.0.0 | Apache-2.0 OR MIT |
| nu-ansi-term | 0.50.3 | MIT |
| num-traits | 0.2.19 | MIT OR Apache-2.0 |
| once_cell | 1.21.4 | MIT OR Apache-2.0 |
| parking | 2.2.1 | Apache-2.0 OR MIT |
| parking_lot | 0.12.5 | MIT OR Apache-2.0 (*) |
| parking_lot_core | 0.9.12 | MIT OR Apache-2.0 |
| password-hash | 0.5.0 | MIT OR Apache-2.0 |
| percent-encoding | 2.3.2 | MIT OR Apache-2.0 |
| pin-project-lite | 0.2.17 | Apache-2.0 OR MIT |
| png | 0.18.1 | MIT OR Apache-2.0 |
| potential_utf | 0.1.6 | Unicode-3.0 |
| ppv-lite86 | 0.2.21 | MIT OR Apache-2.0 |
| proc-macro2 | 1.0.107 | MIT OR Apache-2.0 (*) |
| pxfm | 0.1.30 | BSD-3-Clause OR Apache-2.0 |
| qrcode | 0.14.1 | MIT OR Apache-2.0 |
| quick-error | 2.0.1 | MIT/Apache-2.0 |
| quote | 1.0.47 | MIT OR Apache-2.0 (*) |
| rand | 0.8.8 | MIT OR Apache-2.0 |
| rand_chacha | 0.3.1 | MIT OR Apache-2.0 |
| rand_core | 0.6.4 | MIT OR Apache-2.0 (*) |
| regex-automata | 0.4.18 | MIT OR Apache-2.0 (*) |
| regex-syntax | 0.8.11 | MIT OR Apache-2.0 |
| rpassword | 7.5.5 | Apache-2.0 |
| rtoolbox | 0.0.6 | Apache-2.0 |
| ryu | 1.0.23 | Apache-2.0 OR BSL-1.0 |
| scopeguard | 1.2.0 | MIT OR Apache-2.0 |
| serde | 1.0.229 | MIT OR Apache-2.0 (*) |
| serde_core | 1.0.229 | MIT OR Apache-2.0 |
| serde_derive | 1.0.229 | MIT OR Apache-2.0 |
| serde_json | 1.0.154 | MIT OR Apache-2.0 |
| serde_path_to_error | 0.1.20 | MIT OR Apache-2.0 |
| serde_urlencoded | 0.7.1 | MIT/Apache-2.0 (*) |
| sha2 | 0.10.9 | MIT OR Apache-2.0 (*) |
| sharded-slab | 0.1.7 | MIT |
| simd-adler32 | 0.3.10 | MIT |
| simdutf8 | 0.1.5 | MIT OR Apache-2.0 |
| slab | 0.4.12 | MIT |
| smallvec | 1.16.5 | MIT OR Apache-2.0 |
| socket2 | 0.6.5 | MIT OR Apache-2.0 (*) |
| spin | 0.9.9 | MIT (*) |
| sqlx | 0.8.6 | MIT OR Apache-2.0 |
| sqlx-core | 0.8.6 | MIT OR Apache-2.0 (*) |
| sqlx-macros | 0.8.6 | MIT OR Apache-2.0 |
| sqlx-macros-core | 0.8.6 | MIT OR Apache-2.0 |
| sqlx-sqlite | 0.8.6 | MIT OR Apache-2.0 |
| stable_deref_trait | 1.2.1 | MIT OR Apache-2.0 |
| subtle | 2.6.1 | BSD-3-Clause |
| syn | 2.0.119 | MIT OR Apache-2.0 (*) |
| syn | 3.0.10 | MIT OR Apache-2.0 (*) |
| sync_wrapper | 1.0.2 | Apache-2.0 |
| synstructure | 0.14.0 | MIT (*) |
| thiserror | 2.0.21 | MIT OR Apache-2.0 (*) |
| thiserror-impl | 2.0.21 | MIT OR Apache-2.0 |
| thread_local | 1.1.10 | MIT OR Apache-2.0 |
| tinystr | 0.8.5 | Unicode-3.0 |
| tokio | 1.54.1 | MIT (*) |
| tokio-macros | 2.7.2 | MIT |
| tokio-stream | 0.1.19 | MIT (*) |
| tokio-util | 0.7.20 | MIT |
| tower | 0.5.3 | MIT (*) |
| tower-http | 0.6.11 | MIT |
| tower-layer | 0.3.3 | MIT |
| tower-service | 0.3.3 | MIT |
| tracing | 0.1.44 | MIT (*) |
| tracing-attributes | 0.1.31 | MIT |
| tracing-core | 0.1.36 | MIT (*) |
| tracing-log | 0.2.0 | MIT |
| tracing-subscriber | 0.3.23 | MIT |
| typenum | 1.20.1 | MIT OR Apache-2.0 |
| unicase | 2.10.0 | MIT OR Apache-2.0 |
| unicode-ident | 1.0.27 | (MIT OR Apache-2.0) AND Unicode-3.0 |
| url | 2.5.8 | MIT OR Apache-2.0 (*) |
| utf8_iter | 1.1.0 | Apache-2.0 OR MIT (*) |
| utf_types | 1.0.0 | Apache-2.0 OR MIT |
| uuid | 1.29.2 | Apache-2.0 OR MIT |
| windows-link | 0.2.1 | MIT OR Apache-2.0 |
| windows-sys | 0.61.2 | MIT OR Apache-2.0 (*) |
| writeable | 0.6.4 | Unicode-3.0 |
| yoke | 0.8.4 | Unicode-3.0 (*) |
| yoke-derive | 0.8.4 | Unicode-3.0 |
| zerocopy | 0.8.63 | BSD-2-Clause OR Apache-2.0 OR MIT |
| zerofrom | 0.1.8 | Unicode-3.0 (*) |
| zerofrom-derive | 0.1.8 | Unicode-3.0 |
| zerotrie | 0.2.5 | Unicode-3.0 (*) |
| zerovec | 0.11.9 | Unicode-3.0 (*) |
| zerovec-derive | 0.11.7 | Unicode-3.0 |
| zmij | 1.0.23 | MIT |
| zune-core | 0.5.3 | MIT OR Apache-2.0 OR Zlib |
| zune-jpeg | 0.5.15 | MIT OR Apache-2.0 OR Zlib |

---

## 3. npm packages (frontend, bundled into the web UI)

| Package | Version | License |
|---|---|---|
| @line/bot-sdk | 10.8.0 | Apache-2.0 |
| @types/node | 24.19.2 | MIT |
| agent-base | 6.0.2 | MIT |
| asynckit | 0.4.0 | MIT |
| axios | 1.21.1 | MIT |
| call-bind-apply-helpers | 1.0.2 | MIT |
| combined-stream | 1.0.8 | MIT |
| cookie | 1.1.1 | MIT |
| debug | 4.4.3 | MIT |
| delayed-stream | 1.0.0 | MIT |
| dunder-proto | 1.0.1 | MIT |
| es-define-property | 1.0.1 | MIT |
| es-errors | 1.3.0 | MIT |
| es-object-atoms | 1.1.2 | MIT |
| es-set-tostringtag | 2.1.0 | MIT |
| follow-redirects | 1.16.3 | MIT |
| form-data | 4.0.6 | MIT |
| function-bind | 1.1.2 | MIT |
| get-intrinsic | 1.3.0 | MIT |
| get-proto | 1.0.1 | MIT |
| gopd | 1.2.0 | MIT |
| has-symbols | 1.1.0 | MIT |
| has-tostringtag | 1.0.2 | MIT |
| hasown | 2.0.4 | MIT |
| https-proxy-agent | 5.0.1 | MIT |
| math-intrinsics | 1.1.0 | MIT |
| mime-db | 1.52.0 | MIT |
| mime-types | 2.1.35 | MIT |
| ms | 2.1.3 | MIT |
| proxy-from-env | 2.1.0 | MIT |
| react | 19.3.1 | MIT |
| react-dom | 19.3.1 | MIT |
| react-router | 7.18.5 | MIT |
| scheduler | 0.28.0 | MIT |
| set-cookie-parser | 2.7.3 | MIT |
| tiny-sha256 | 1.0.2 | Public domain |
| tslib | 2.9.1 | 0BSD |
| undici-types | 7.24.6 | MIT |
| whatwg-fetch | 3.6.20 | MIT |

---

## 4. Container base images / 容器基底映像

The official container image is built on `debian:bookworm-slim` and includes Debian packages (e.g. `ca-certificates`, `curl`) that are licensed under their own terms; see `/usr/share/doc/<package>/copyright` inside the image. / 官方容器映像以 `debian:bookworm-slim` 為基底，內含 Debian 套件（如 `ca-certificates`、`curl`），各依其授權條款提供，授權資訊見映像內 `/usr/share/doc/<package>/copyright`。
