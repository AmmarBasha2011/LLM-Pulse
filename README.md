# LLM Pulse (LiteLLM Endpoint Inspector)

**LLM Pulse** is a high-performance, bilingual (English / Arabic) web application built for validating, benchmarking, and testing LiteLLM routing configurations (`litellm_config.yaml`) directly in the browser.

## 🚀 Key Features

1. **Bilingual UI (AR / EN)**: Instant language switching with dynamic RTL/LTR document layout, Cairo typography for Arabic, Inter for English, and JetBrains Mono for code and latency metrics.
2. **YAML Parsing Engine**: Drag-and-drop file upload (`.yaml`, `.yml`, `.txt`), raw YAML pasting, and a built-in sample config loader for instant testing.
3. **Concurrent Testing Engine**: 
   - Async worker pool with adjustable concurrency (`1`, `3`, `5`, `10` workers).
   - Configurable request timeouts (`5s`, `10s`, `20s`, `30s` via `AbortController`).
   - Stop testing controls and real-time progress indicators.
   - Smart request formatting (strips LiteLLM routing prefixes like `openai/`, handles Cloudflare Workers AI URL paths, supports optional CORS proxies).
4. **Interactive Dashboard & Analytics**:
   - Live summary counters (Total, Working, Failed, Pending, Fastest Provider).
   - Recharts latency bar chart for visual performance comparison across working endpoints.
   - Live search filtering, status pills, and provider dropdown filters.
5. **Advanced Diagnostics & Latency History**:
   - Color-coded latency threshold system (`<500ms` Green, `500-1500ms` Yellow, `>1500ms` Red).
   - Tracks the last 3 test results per endpoint with visual sparkline trend charts in the View Details modal.
   - Detailed error diagnostics and server response inspectors with one-click API key copying.
6. **Flexible Exporting**:
   - Export verified working configurations as a clean `.yaml` file.
   - Custom CSV export modal with selective column toggling (Model Name, Provider, Status, Latency, API Base, etc.).

---

## 🛠️ Tech Stack

- **Framework**: React 19 + TypeScript on Vite
- **Styling**: Tailwind CSS v4
- **Icons**: Lucide Icons
- **Parsing**: `js-yaml`
- **Charts**: Recharts

---

## 📦 Local Development & Deployment

1. **Install Dependencies**:
   ```bash
   npm install
   ```

2. **Run Development Server**:
   ```bash
   npm run dev
   ```

3. **Build for Production**:
   ```bash
   npm run build
   ```

4. **Deploy on Vercel**:
   This project is pre-configured with `vercel.json` for one-click deployment on Vercel. Simply import the repository into Vercel and deploy!
