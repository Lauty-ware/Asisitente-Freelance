#  FreelanceSales AI — Asistente de Ventas para Freelancers

> El copiloto que ayuda a freelancers a **vender más, en menos tiempo y sin olvidar seguimientos**.

![Estado](https://img.shields.io/badge/estado-MVP%20en%20desarrollo-yellow)
![Licencia](https://img.shields.io/badge/licencia-MIT-blue)
![Versión](https://img.shields.io/badge/versión-0.1.0-green)

---

## 📖 Tabla de Contenidos

1. [¿Qué es FreelanceSales AI?](#-qué-es-freelancesales-ai)
2. [El Problema que Resuelve](#-el-problema-que-resuelve)
3. [Funcionalidades](#-funcionalidades)
4. [Stack Tecnológico](#-stack-tecnológico)
5. [Instalación](#-instalación)
6. [Configuración](#-configuración)
7. [Uso Rápido](#-uso-rápido)
8. [Estructura del Proyecto](#-estructura-del-proyecto)
9. [API de IA (Prompts)](#-api-de-ia-prompts)
10. [Roadmap](#-roadmap)
11. [Contribuir](#-contribuir)
12. [Licencia](#-licencia)
13. [Contacto](#-contacto)

---

## 🎯 ¿Qué es FreelanceSales AI?

**FreelanceSales AI** es un asistente de ventas diseñado específicamente para **freelancers** (diseñadores, developers, redactores, consultores, fotógrafos, marketers, etc.) que necesitan gestionar su pipeline comercial sin la complejidad de un CRM corporativo.

Combina:
- 📋 **Gestión simple de leads**
- 💰 **Cotizador inteligente**
- 🤖 **IA para redactar emails y propuestas**
- ⏰ **Recordatorios automáticos de seguimiento**
- 📊 **Métricas básicas de conversión**

---

## 🔥 El Problema que Resuelve

Los freelancers suelen:

- ❌ Perder leads por olvidar hacer seguimiento
- ❌ Invertir horas redactando propuestas desde cero
- ❌ No saber cuánto cobrar o cómo negociar
- ❌ Usar hojas de cálculo o post-its como CRM
- ❌ Pagar herramientas caras con funciones que no usan

**FreelanceSales AI** resuelve esto con una interfaz mínima, foco en velocidad y asistencia de IA en cada paso del ciclo de venta.

---

## ✨ Funcionalidades

### 📋 Gestión de Leads
- Alta rápida de prospectos (nombre, email, origen, notas)
- Estados del pipeline: `Nuevo → Contactado → Propuesta → Negociación → Cerrado / Perdido`
- Vista **Kanban** arrastrable
- Historial de interacciones por lead
- Etiquetas personalizadas (ej: "urgente", "presupuesto bajo")

### 💰 Cotizador Inteligente
- Cálculo automático basado en **horas estimadas × tarifa horaria**
- Plantillas de propuestas reutilizables
- Exportación a **PDF** con tu branding
- Sugerencia de precio según tipo de proyecto (IA)

### 🤖 Asistencia con IA
- **Redacción de emails** de prospección, seguimiento y cierre
- **Respuestas a objeciones** ("es muy caro", "lo tengo que pensar")
- **Resumen de historial** de un cliente antes de una llamada
- **Generación de propuestas** a partir de un briefing corto
- **Detección de señales de compra** en conversaciones

### ⏰ Seguimiento Automatizado
- Recordatorios configurables (ej: "si no responde en 3 días, avísame")
- Cola de tareas diarias ("hoy debes contactar a 4 leads")
- Emails sugeridos listos para copiar/pegar o enviar

### 📊 Análisis Básico
- Tasa de conversión por etapa
- Ticket promedio
- Tiempo medio de cierre
- Origen de leads más rentable

### 🔒 Extras
- Multi-idioma (ES/EN)
- Modo oscuro
- Exportación de datos (CSV/JSON)
- Sin lock-in: tus datos son tuyos

---

## 🛠 Stack Tecnológico

| Capa | Tecnología |
|------|------------|
| **Frontend** | Next.js 14 + React + Tailwind CSS |
| **Backend** | Supabase (Auth + Postgres + Storage) |
| **IA** | OpenAI API (GPT-4o-mini) / Claude API |
| **Emails** | Resend |
| **PDF** | react-pdf |
| **Deploy** | Vercel |
| **Testing** | Vitest + Playwright |

> 💡 ¿Prefieres low-code? Hay una rama `lowcode/` con Bubble + Airtable + Make para validar rápido.

---

## ⚙️ Instalación

### Requisitos previos
- Node.js ≥ 18
- npm / pnpm / yarn
- Cuenta en [Supabase](https://supabase.com) (gratis)
- API Key de [OpenAI](https://platform.openai.com) o [Anthropic](https://console.anthropic.com)

### Pasos

```bash
# 1. Clonar el repositorio
git clone https://github.com/tu-usuario/freelance-sales-ai.git
cd freelance-sales-ai

# 2. Instalar dependencias
npm install

# 3. Copiar variables de entorno
cp .env.example .env.local

# 4. Configurar variables (ver sección siguiente)

# 5. Ejecutar migraciones de la base de datos
npm run db:migrate

# 6. Iniciar en modo desarrollo
npm run dev