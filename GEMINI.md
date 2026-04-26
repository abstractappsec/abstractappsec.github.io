# Gemini Guidelines: Abstract AppSec

## Core Mandate: Content Integrity
- **Content Authoring:** The AI assistant is strictly prohibited from authoring or generating primary content, articles, posts, or narratives for this site. 
- **AI Role:** The AI's role is exclusively limited to **formatting, styling, and structural implementation**. This includes:
  - Markdown formatting (tables, lists, headers).
  - CSS/Sass styling and theme configuration.
  - Jekyll layout structure and Liquid templating.
  - Organization of files and folders for the site's architecture.
- **Content Policy:** All site content (posts, descriptions, intros) will be written entirely by the author. If a placeholder is needed, it must be a simple "TODO" or empty file.

## Web Development Best Practices

### 1. Performance & Optimization
- **Asset Minification:** Ensure CSS and JS are minified where possible.
- **Image Optimization:** Use modern formats (WebP) and ensure images are sized correctly for their containers.
- **Minimize Dependencies:** Keep the `Gemfile` lean to speed up build times.

### 2. Accessibility (a11y)
- **Semantic HTML:** Use proper tags (`<nav>`, `<main>`, `<aside>`, `<article>`) to ensure screen readers can navigate the site.
- **Alt Text:** Always provide descriptive `alt` text for images.
- **Contrast:** Maintain high color contrast (following Dracula theme standards) for readability.

### 3. Maintainability
- **Surgical Edits:** Use targeted changes rather than overwriting entire files when possible.
- **Consistent Styling:** Adhere strictly to the Dracula color palette and typography.
- **Clean Liquid Logic:** Keep Jekyll templates readable and avoid overly complex Liquid logic where a simpler structure would suffice.

### 4. Security
- **No Analytics:** Do not include Google Analytics or other tracking scripts.
- **Dependency Audits:** Periodically check gems for security vulnerabilities.
- **Environment Safety:** Never expose sensitive configuration in the repository.

## Workflow
1. **Author** creates raw content.
2. **Gemini** assists with formatting into the correct Jekyll structure and applying styles.
3. **Verification** via local `bundle exec jekyll serve` before any deployment.
