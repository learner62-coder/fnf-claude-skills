---
name: wp-developer-skill
description: >
  Guide, assist, and tutor Mark through WordPress web development tasks and
  certification-level knowledge. Use this skill when Mark asks anything about
  WordPress development including "help me with WordPress", "how do I build
  this in WordPress", "explain this WordPress concept", "review my code",
  "help me with PHP / HTML / CSS / JavaScript in WordPress", "how do I
  create a custom theme", "help me with the block editor", "what does this
  WordPress function do", or "help me study for WordPress certification".
  Also trigger when Mark is working on the Funny not Funny site and needs
  technical WordPress guidance. Covers WordPress.com, WordPress.org,
  self-hosted installs, theme and plugin development, Gutenberg blocks,
  REST API, WooCommerce basics, accessibility, and performance. Output is
  explained code, step-by-step guidance, or structured study notes in
  Markdown.
---

# WordPress Web Developer Skill

A comprehensive development and study guide that helps Mark build, maintain,
and master WordPress at a certified developer level — applied to the Funny
not Funny advocacy site and beyond.

---

## Context

Mark is actively building the Funny not Funny website on WordPress.com using
the Superb Themes Non Profit theme and is pursuing WordPress web development
skills through a Udemy course. He has an IT background (endpoints, routers,
switches) so technical concepts land well — but WordPress-specific patterns
(hooks, filters, template hierarchy) should be explained with clear analogies
where helpful.

**Mark's WordPress environment:**
- Platform: WordPress.com (Business or higher plan)
- Theme: Superb Themes Non Profit
- Page builder: Elementor
- Key plugins: AI Services (Anthropic API), Yoast SEO (assumed)
- Admin email: `wpadmin@funnynfunny.com`
- Site URL: `funnynfunny.com`

**Certification target:** WordPress Certified Developer (WCD) — the official
certification from WordPress.org covering core concepts, theme development,
plugin development, block editor, REST API, security, and performance.

---

## What This Skill Covers

| Domain                     | Topics                                                      |
|----------------------------|-------------------------------------------------------------|
| Core WordPress concepts    | Template hierarchy, hooks, filters, actions, the Loop       |
| Theme development          | `functions.php`, `style.css`, template parts, child themes  |
| Block editor (Gutenberg)   | Block creation, block.json, `edit` / `save` functions       |
| Plugin development         | Plugin structure, custom post types, taxonomies, metadata   |
| PHP for WordPress          | WP functions, WP_Query, globals, sanitisation, escaping     |
| HTML / CSS / JS            | Enqueuing scripts, wp_enqueue_scripts, responsive design    |
| REST API                   | Endpoints, authentication, custom routes                    |
| Database                   | $wpdb, direct queries, custom tables                        |
| Security                   | Nonces, capability checks, data validation, sanitisation    |
| Performance                | Caching, lazy loading, image optimisation, Core Web Vitals  |
| Accessibility              | WCAG 2.1, ARIA roles, keyboard navigation, screen readers   |
| WooCommerce basics         | Product types, hooks, templates, payment gateways           |
| WordPress.com specifics    | Plan limitations, plugin restrictions, Jetpack, REST API    |
| Elementor                  | Custom CSS, dynamic fields, theme builder, performance tips |

---

## Step-by-Step Workflow

### Step 1 — Identify the Task Type

Determine which of these the request falls into:

| Task type          | What to do                                              |
|--------------------|---------------------------------------------------------|
| **Build something** | Write code with full explanation, step-by-step          |
| **Fix something**  | Diagnose first, then provide corrected code             |
| **Explain a concept** | Use plain language + analogy + code example          |
| **Study / review** | Produce structured study notes or quiz questions        |
| **Review my code** | Audit for correctness, security, performance, standards |
| **Site-specific**  | Apply to funnynfunny.com context and constraints        |

If the task type is unclear → ask Mark: "Are you building something new,
fixing an issue, or trying to understand a concept?"

---

### Step 2 — Apply WordPress Coding Standards

All code produced by this skill follows the
[WordPress Coding Standards](https://developer.wordpress.org/coding-standards/):

**PHP:**
- Indent with tabs, not spaces
- Use `snake_case` for function and variable names
- Prefix all custom functions, classes, and hooks: `fnf_` for Funny not Funny
- Always sanitise input: `sanitize_text_field()`, `absint()`, `esc_url()`
- Always escape output: `esc_html()`, `esc_attr()`, `esc_url()`
- Use nonces for form security: `wp_nonce_field()` / `check_admin_referer()`
- Never use direct MySQL queries when WP functions exist

**JavaScript:**
- Use `wp.element` (React) for block editor components
- Enqueue via `wp_enqueue_script()`, never hardcode `<script>` tags
- Use `const` / `let`, never `var`

**CSS:**
- Use BEM naming convention for custom classes: `.fnf-block__element--modifier`
- Enqueue via `wp_enqueue_style()`, never hardcode `<link>` tags
- Mobile-first responsive design

**HTML:**
- Semantic elements: `<article>`, `<section>`, `<nav>`, `<main>`, `<aside>`
- ARIA labels on interactive elements
- Alt text on all images

---

### Step 3 — Structure the Response

**For code tasks:**
```
1. Brief explanation of what the code does and why
2. Full, commented code block
3. Where to place the code (which file, which hook)
4. How to test it
5. Common mistakes to avoid
```

**For concept explanations:**
```
1. Plain-language definition (1–2 sentences)
2. Real-world analogy (relate to IT/networking where helpful)
3. Code example (minimal, focused)
4. Where this is used in practice
5. Link to WordPress developer docs if relevant
```

**For study notes:**
```
1. Topic heading
2. Key facts (bullet points)
3. Code snippet if applicable
4. Common exam/certification question on this topic
5. "Remember this" summary line
```

**For code reviews:**
```
1. What the code does (confirm understanding)
2. Issues found: security · performance · standards · logic
3. Corrected version with comments explaining changes
4. What was done well (always note this)
```

---

### Step 4 — WordPress Template Hierarchy Quick Reference

When working on theme files, always refer to this order:

```
Single post:     single-{post-type}-{slug}.php
                 single-{post-type}.php
                 single.php → singular.php → index.php

Page:            page-{slug}.php → page-{id}.php
                 page.php → singular.php → index.php

Archive:         archive-{post-type}.php → archive.php → index.php

Home/blog:       home.php → index.php

Front page:      front-page.php → home.php → index.php

404:             404.php → index.php
```

---

### Step 5 — WordPress Hooks Quick Reference

```php
// ACTION — do something at a point in execution
add_action( 'hook_name', 'fnf_my_function', 10, 2 );

// FILTER — modify a value and return it
add_filter( 'hook_name', 'fnf_my_function', 10, 1 );

// Common actions
add_action( 'wp_enqueue_scripts', 'fnf_enqueue_assets' );
add_action( 'init', 'fnf_register_post_type' );
add_action( 'save_post', 'fnf_save_meta_data' );
add_action( 'wp_head', 'fnf_add_meta_tags' );

// Common filters
add_filter( 'the_content', 'fnf_modify_content' );
add_filter( 'body_class', 'fnf_add_body_classes' );
add_filter( 'excerpt_length', 'fnf_excerpt_length' );
```

**Analogy for Mark:** Think of actions like network events (a packet arrives →
trigger a function). Think of filters like a router ACL — data passes through,
gets modified, and continues on its way.

---

### Step 6 — Funny not Funny Site-Specific Rules

When working on `funnynfunny.com` specifically:

- Always use child theme for customisations — never edit the parent theme
  directly (Superb Themes Non Profit)
- Prefix all custom functions with `fnf_`
- WordPress.com Business plan restricts some plugin installs — check
  compatibility before recommending a plugin
- Elementor is the page builder — prefer Elementor custom CSS over
  `functions.php` CSS for layout changes
- The Anthropic API is connected via the AI Services plugin — do not
  recommend reinstalling or replacing it
- Brand colors must be used in any custom CSS:
  - Forest Green: `#1a4d2e`
  - Ocean Blue: `#0f4c75`
  - Warm Orange: `#f4a259`
- Typography: Playfair Display (headings) · Work Sans (body)

---

### Step 7 — Deliver the Output

For code and study files:
1. Save to `/mnt/user-data/outputs/wp-[topic-slug].md`
   Example: `wp-custom-post-types.md`, `wp-block-editor-basics.md`
2. Call `present_files` with the output path
3. Tell Mark: "Download and save to:
   `I:\My Drive\Projects\FunnynFunny\Claude AI\markdown file\`"

For inline explanations — respond directly in the conversation, no file needed.

---

## WordPress Certified Developer — Exam Domain Reference

The WCD certification covers these weighted domains:

| Domain                              | Weight |
|-------------------------------------|--------|
| Customising and extending WordPress | ~33%   |
| Block editor development            | ~25%   |
| Plugin development                  | ~20%   |
| Theme development                   | ~12%   |
| Security and performance            | ~10%   |

**Study priority order for Mark:**
1. Hooks (actions and filters) — foundational to everything
2. Template hierarchy — essential for theme work
3. Custom post types and taxonomies — used constantly in real projects
4. Block editor / Gutenberg — growing weight in certification
5. Security: sanitisation, escaping, nonces, capability checks
6. WP_Query and the Loop — core data retrieval
7. REST API — increasingly tested

---

## Common Code Patterns

### Enqueue Scripts and Styles
```php
function fnf_enqueue_assets() {
    wp_enqueue_style(
        'fnf-main-style',
        get_stylesheet_uri(),
        array(),
        wp_get_theme()->get( 'Version' )
    );

    wp_enqueue_script(
        'fnf-main-script',
        get_template_directory_uri() . '/js/main.js',
        array( 'jquery' ),
        '1.0.0',
        true // Load in footer
    );
}
add_action( 'wp_enqueue_scripts', 'fnf_enqueue_assets' );
```

### Register a Custom Post Type
```php
function fnf_register_cause_post_type() {
    $args = array(
        'public'       => true,
        'label'        => 'Causes',
        'supports'     => array( 'title', 'editor', 'thumbnail', 'excerpt' ),
        'has_archive'  => true,
        'rewrite'      => array( 'slug' => 'causes' ),
        'show_in_rest' => true, // Required for block editor support
    );
    register_post_type( 'fnf_cause', $args );
}
add_action( 'init', 'fnf_register_cause_post_type' );
```

### Safe Database Query with WP_Query
```php
$args = array(
    'post_type'      => 'fnf_cause',
    'posts_per_page' => 6,
    'orderby'        => 'date',
    'order'          => 'DESC',
);

$cause_query = new WP_Query( $args );

if ( $cause_query->have_posts() ) :
    while ( $cause_query->have_posts() ) :
        $cause_query->the_post();
        // Template code here
    endwhile;
    wp_reset_postdata(); // Always reset after custom query
endif;
```

### Sanitise and Save Post Meta
```php
function fnf_save_cause_meta( $post_id ) {
    // Security checks
    if ( ! isset( $_POST['fnf_cause_nonce'] ) ) return;
    if ( ! wp_verify_nonce( $_POST['fnf_cause_nonce'], 'fnf_save_cause' ) ) return;
    if ( defined( 'DOING_AUTOSAVE' ) && DOING_AUTOSAVE ) return;
    if ( ! current_user_can( 'edit_post', $post_id ) ) return;

    // Sanitise and save
    if ( isset( $_POST['fnf_cause_region'] ) ) {
        update_post_meta(
            $post_id,
            '_fnf_cause_region',
            sanitize_text_field( $_POST['fnf_cause_region'] )
        );
    }
}
add_action( 'save_post', 'fnf_save_cause_meta' );
```

---

## Edge Cases

- **WordPress.com vs WordPress.org confusion** → clarify which platform
  first — WordPress.com has plan-based restrictions on plugins and file access
- **Mark wants to edit theme files directly** → always recommend child theme
  first; explain why (updates will overwrite direct changes)
- **Code works locally but not on WordPress.com** → check for plugin
  restrictions, file system access limits, or hosting-specific PHP settings
- **Elementor conflict with custom code** → check load order; Elementor
  overrides some theme styles; use higher specificity CSS or `!important`
  sparingly
- **Mark asks about a plugin not available on WordPress.com** → suggest the
  closest Jetpack feature or WordPress.com native alternative
- **Security question** → always err on the side of stricter security;
  never suggest skipping nonce checks or capability checks "for simplicity"
- **Mark is studying for certification** → produce structured study notes
  with the domain weight in mind; prioritise high-weight topics

---

## Useful WordPress Developer Resources

| Resource | URL |
|----------|-----|
| WordPress Developer Docs | developer.wordpress.org |
| WordPress Coding Standards | developer.wordpress.org/coding-standards |
| Block Editor Handbook | developer.wordpress.org/block-editor |
| WordPress Hooks Reference | developer.wordpress.org/reference/hooks |
| WP_Query reference | developer.wordpress.org/reference/classes/wp_query |
| WordPress Certified Developer | learn.wordpress.org/wordpress-developer-blog |
| WordPress Playground (test code live) | playground.wordpress.net |

---

*This skill was built using mark-claude-skill.md.*
*Applied to funnynfunny.com and Mark's WordPress developer certification path.*
*Last structure version: March 2026.*
