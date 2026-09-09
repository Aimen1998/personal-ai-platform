# Personal AI Platform

طبقة استرجاع وذاكرة وحوكمة تُركَّب على أي agent عبر MCP.
تعمل محليًا بالكامل — لا بيانات تغادر الجهاز.

## الحالة
**Phase 0 مكتمل** — خط أساس يعمل: Hermes Agent + Ollama محلي

## المعمارية
الـcore يقف **بجانب** الوكيل لا أمامه. وجهان لنفس الخدمة:
- **شمالًا:** OpenAI-compatible API — للواجهات
- **جانبًا:** MCP server — للوكلاء (Hermes وغيره)

## Non-goals
لا agent loop · لا chat UI · لا vector DB · لا sandbox خاص.
كلها محلولة في مشاريع ناضجة — نستخدمها ولا نعيد بناءها.

## القرارات المعمارية
[docs/adr/](docs/adr/) — ستة قرارات موثّقة بأسبابها وبدائلها المرفوضة.

## البيئة
Mac M1 · 16 GB · VRAM مقاسة 10.7 GiB
النموذج: `qwen3-agent` @64K — انظر [deploy/](deploy/)# personal-ai-platform
