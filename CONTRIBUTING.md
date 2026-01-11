# Contributing to GSAP ScrollTrigger Showcase

First off, thank you for considering contributing to this project! 🎉

## How Can I Contribute?

### Reporting Bugs

Before creating bug reports, please check existing issues to avoid duplicates. When creating a bug report, include:

- **Clear descriptive title**
- **Exact steps to reproduce**
- **Expected behavior**
- **Actual behavior**
- **Screenshots** (if applicable)
- **Browser and version**

### Suggesting Enhancements

Enhancement suggestions are tracked as GitHub issues. When creating an enhancement suggestion, include:

- **Clear descriptive title**
- **Detailed explanation** of the proposed functionality
- **Why this enhancement would be useful**
- **Examples** of how it would work

### Adding New Scroll Effects

We're always looking for new creative scroll animation techniques! To add a new effect:

1. Create a new section in `index.html`
2. Add corresponding CSS styles
3. Implement the GSAP/ScrollTrigger JavaScript
4. Update the README.md with the new effect
5. Ensure it works on mobile devices
6. Test performance (60fps target)

### Pull Requests

1. **Fork** the repository
2. **Create a branch** from `main`
   ```bash
   git checkout -b feature/amazing-new-effect
   ```
3. **Make your changes**
   - Write clean, commented code
   - Follow existing code style
   - Test on multiple browsers
4. **Commit** with clear messages
   ```bash
   git commit -m "Add parallax zoom effect"
   ```
5. **Push** to your fork
   ```bash
   git push origin feature/amazing-new-effect
   ```
6. **Open a Pull Request**

## Code Style Guidelines

### HTML

- Use semantic HTML5 elements
- Indent with 4 spaces
- Use meaningful class names
- Keep structure clean and organized

### CSS

- Use meaningful class names (BEM methodology preferred)
- Group related properties together
- Comment complex styles
- Use CSS custom properties for repeated values
- Mobile-first approach

### JavaScript

- Use modern ES6+ syntax
- Comment complex logic
- Use meaningful variable names
- Keep functions focused and small
- Handle errors gracefully

### Performance

- Optimize for 60fps
- Use `transform` and `opacity` for animations
- Minimize DOM manipulation
- Test on lower-end devices
- Avoid unnecessary `will-change` usage

## Testing Checklist

Before submitting a PR, ensure:

- [ ] Works in Chrome, Firefox, Safari, Edge
- [ ] Responsive on mobile devices
- [ ] Smooth 60fps performance
- [ ] No console errors
- [ ] Code is commented
- [ ] README.md updated (if needed)
- [ ] Follows existing code style

## Code of Conduct

### Our Standards

- Be respectful and inclusive
- Accept constructive criticism
- Focus on what's best for the community
- Show empathy towards others

### Unacceptable Behavior

- Trolling or insulting comments
- Personal or political attacks
- Harassment of any kind
- Publishing others' private information

## Questions?

Feel free to open an issue with the `question` label or reach out to the maintainers.

## Attribution

This Contributing guide is adapted from open source contribution guidelines.

---

Thank you for contributing! 🚀
