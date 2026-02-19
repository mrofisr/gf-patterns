# GF Patterns

A comprehensive collection of patterns for [gf](https://github.com/tomnomnom/gf), a wrapper around grep to help you find interesting things in code, logs, and web traffic. This repository has been recently updated and cleaned to include modern patterns for AI services, cloud infrastructure, and secrets.

## Installation

1. Ensure you have [gf](https://github.com/tomnomnom/gf) installed:
   ```bash
   go install github.com/tomnomnom/gf@latest
   ```

2. Clone this repository or copy the patterns to your `~/.gf` directory:
   ```bash
   mkdir -p ~/.gf
   git clone https://github.com/mrofisr/gf-patterns
   cp gf-patterns/*.json ~/.gf
   ```

## Usage

List all available patterns:
```bash
gf -list
```

Run a pattern against a file or directory:
```bash
cat file.txt | gf xss
# or
gf aws-keys .
```

## Pattern Catalog

### 🚀 AI & Modern Services (New!)
| Pattern | Description |
|---------|-------------|
| `ai-services` | Comprehensive detection for OpenAI, Anthropic, HuggingFace, Replicate, and xAI tokens. |
| `anthropic` | Focused detection for Anthropic API keys. |
| `cohere` | Detection for Cohere API keys. |
| `groq` | Detection for Groq API keys. |
| `discord-webhooks` | Discord webhook URLs. |
| `slack-webhook_secrets` | Slack incoming webhook URLs. |

### 🔑 Secrets & API Keys
| Pattern | Description |
|---------|-------------|
| `aws-keys` | AWS Access Key IDs (AKIA, etc.) and Secret Access Keys. |
| `github_secrets` | GitHub Personal Access Tokens (ghp, gho, ghu, ghs, ghr). |
| `google-keys_secrets` | Google API Keys (AIza...). |
| `heroku-keys_secrets` | Heroku API keys. |
| `stripe-keys_secrets` | Stripe Secret and Publishable keys. |
| `npm-tokens` | NPM authentication tokens. |
| `pypi-tokens` | PyPI upload tokens. |
| `firebase_secrets` | Firebase database URLs and secrets. |
| `jwt` | JSON Web Tokens (base64 encoded). |
| `asymmetric-keys_secrets`| RSA/SSH Private Keys. |
| `facebook-token_secrets` | Facebook Access Tokens. |
| `twitter-token_secrets` | Twitter OAuth tokens. |

### 🛡️ Vulnerabilities
| Pattern | Description |
|---------|-------------|
| `sqli` | Potential SQL injection parameters and patterns. |
| `xss` | Cross-Site Scripting (XSS) triggers and parameters. |
| `ssrf` | Server-Side Request Forgery (SSRF) target parameters. |
| `lfi` | Local File Inclusion (LFI) target parameters and paths. |
| `rce` | Remote Code Execution (RCE) sinks and parameters. |
| `ssti` | Server-Side Template Injection (SSTI) patterns. |
| `idor` | Potential IDOR (Insecure Direct Object Reference) parameters. |
| `redirect` | Open redirect parameters and patterns. |
| `takeovers` | Fingerprints for subdomain takeovers (S3, GitHub Pages, etc.). |
| `cors` | Potential CORS misconfiguration indicators. |

### ☁️ Infrastructure & Cloud
| Pattern | Description |
|---------|-------------|
| `cloud-resources` | Subdomains for Cloudfront, Elastic Beanstalk, Azure Blobs, GCP Storage, etc. |
| `s3-buckets` | AWS S3 bucket URLs. |
| `servers` | Common server headers and IP addresses. |
| `ip` | IPv4 and IPv6 address patterns. |
| `fw` | Firewall and networking related patterns. |

### 📂 Files & Frameworks
| Pattern | Description |
|---------|-------------|
| `sensitive-files` | Sensitive filenames like `.env`, `.git/config`, `wp-config.php`, etc. |
| `modern-frameworks` | Next.js, Nuxt, and various lock files. |
| `api-endpoints` | API versioning, GraphQL, Swagger, and OpenAPI endpoints. |
| `openapi` | OpenAPI/Swagger definitions. |

### 🛠️ Development & Misc
| Pattern | Description |
|---------|-------------|
| `interestingparams` | Mega-list of interesting parameters for security testing. |
| `interestingEXT` | Interesting file extensions. |
| `interestingsubs` | Interesting subdomains. |
| `php-*` | Various PHP sinks, sources, and error patterns. |
| `go-functions` | Common Go function definitions. |
| `debug-pages` | Common debug and development pages. |
| `badwords` | Comments indicating hacks, TODOs, or insecure code. |

## Credits

Special thanks to [Tomnomnom](https://github.com/tomnomnom) for creating `gf`.
Many patterns are collected and refined from various community sources including [1ndianl33t](https://github.com/1ndianl33t/Gf-Patterns).
