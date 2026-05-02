# PDF → Markdown | RAG Builder

**Convierte PDFs a Markdown limpio para indexar en un corpus RAG jurídico.**

App estática 100% en el navegador — sin servidor, sin instalación, sin costo.

🔗 **Demo en vivo:** https://gaboazmx.github.io/pdf2md/

---

## ¿Para qué sirve?

Forma parte del ecosistema **Sistema RAG Jurídico** del Despacho Gabriel Aranda Zamacona. Permite transformar leyes, libros, resoluciones y doctrina jurídica en formato Markdown listo para indexar con `indexar.py`.

El flujo completo es:

```
PDF  →  [esta app]  →  .md  →  corpus\categoria\  →  python indexar.py  →  RAG consultable desde Cowork
```

---

## Características

- **Drag & drop** — arrastra uno o varios PDFs a la vez
- **Detección automática de estructura jurídica** — convierte ARTÍCULO, CAPÍTULO, TÍTULO, FRACCIÓN a encabezados Markdown
- **Metadatos YAML** — bloque `---` al inicio con fuente, categoría, páginas y fecha
- **Selector de categoría** — 24 categorías del corpus jurídico preconfiguradas
- **Vista previa** — modo Markdown crudo y modo renderizado
- **Descarga individual o en lote** — un `.md` por PDF, con nombre limpio
- **Funciona offline** — solo necesitas el archivo `index.html`

---

## Uso

### Opción A — En línea
Entra a https://gaboazmx.github.io/pdf2md/ y úsala directamente.

### Opción B — Local (offline)
```bash
git clone https://github.com/gaboazmx/pdf2md.git
# Abrir index.html en cualquier navegador moderno
```

No requiere Node, Python ni ninguna dependencia adicional.

---

## Limitaciones

- Solo funciona con PDFs que tengan **texto seleccionable** (no escaneados)
- Para PDFs escaneados: aplicar OCR primero con Adobe Acrobat → Herramientas → Reconocer texto
- La calidad del Markdown depende de la estructura interna del PDF

---

## Integración con el Sistema RAG

Una vez generados los archivos `.md`:

1. Copiarlos a la carpeta de corpus correspondiente:
   ```
   C:\Users\gabri\Dropbox\gabriel_rag\corpus\[categoria]\
   ```

2. Indexar:
   ```powershell
   cd C:\Users\gabri\Dropbox\gabriel_rag
   python indexar.py --cat "[categoria]"
   ```

3. Consultar desde Cowork con la skill `rag-corpus-gabriel`.

---

## Repositorio principal del Sistema RAG

El sistema completo de indexación y consulta está en:
[github.com/gaboazmx/gabriel-rag](https://github.com/gaboazmx/gabriel-rag) *(próximamente)*

---

## Autor

**Gabriel Aranda Zamacona**
Abogado Corporativo · Litigante Contencioso Administrativo Federal · Estratega Legal con IA

---

*Despacho Gabriel Aranda Zamacona — Abril 2026*
