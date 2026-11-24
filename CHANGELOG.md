## rj-default Theme v1.0.5

### 🐛 Fixed
- **Comment form 404 on translated slugs:** Both reply and main comment forms in `single-post.blade.php` now use `url()->current() . '/comment'` instead of `route('frontend.comments.store', $post)`, ensuring comments work correctly on posts accessed via translated slugs.

- **Comment form mobile layout:** Replaced Tailwind grid classes with the theme's native `.rj-form-row` class. Name and email fields now stack vertically below 768px, preventing overflow on mobile devices.

### 🔧 Changed
- **`single-post.blade.php`:** Comment form action extracted into a single `$commentAction` variable, reused by both the reply form and the primary comment form to keep markup consistent.

### 📦 Upgrade Notes
- No database migrations required.
- No breaking changes. Safe drop-in replacement for v1.0.4.
