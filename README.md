# SASS-Collection

A comprehensive SASS styling library that provides a unified design language through modular, composable styles. This library combines a style guide with a component library to create a flexible, maintainable design system.

## Features

- 🎨 Comprehensive design token system
- 📱 Responsive design utilities
- 🧩 Modular component architecture
- 🌗 Theme support (light/dark)
- 🛠 Utility-first approach with component patterns
- 📦 Zero-dependency pure SASS
- 🔧 Highly customizable
- 📚 Well-documented patterns and usage

## Installation

```bash
# Via npm
npm install @9kenm/sass-collection

# Via yarn
yarn add @9kenm/sass-collection
```

## Usage

### Basic Import
```scss
// Import everything
@import "@9kenm/sass-collection/sass/main";

// Import specific modules
@import "@9kenm/sass-collection/sass/abstracts/variables";
@import "@9kenm/sass-collection/sass/components/atoms/buttons";
```

### Using Components
```scss
.my-component {
  @include responsive-container();
  @include spacing(md);
  
  // Use design tokens
  color: var(--color-primary-600);
  font-size: var(--text-size-lg);
  
  // Extend existing patterns
  @extend %card-shadow;
  
  // Responsive patterns
  @include breakpoint(md) {
    @include grid(2);
  }
}
```

## Architecture

```
sass/
├── abstracts/               # Core functionality
│   ├── _variables.scss     # Global variables
│   ├── _functions.scss     # Custom SASS functions
│   ├── _mixins.scss       # Reusable mixins
│   └── _tokens.scss       # Design tokens
├── base/                   # Base styles
│   ├── _reset.scss        # CSS reset/normalize
│   ├── _typography.scss   # Typography rules
│   ├── _animations.scss   # Global animations
│   └── _utilities.scss    # Utility classes
├── layout/                 # Layout patterns
│   ├── _grid.scss        # Grid system
│   ├── _spacing.scss     # Spacing helpers
│   ├── _containers.scss  # Container layouts
│   └── _positioning.scss # Position helpers
├── components/            # Component styles
│   ├── atoms/            # Basic components
│   ├── molecules/        # Combined components
│   └── organisms/        # Complex components
├── themes/                # Theme variations
│   ├── _light.scss      # Light theme
│   └── _dark.scss       # Dark theme
└── main.scss             # Main entry file
```

## Best Practices

### Naming Conventions
- Use BEM methodology for components: `.block__element--modifier`
- Prefix utilities with `u-`: `.u-margin-top`
- Prefix mixins with purpose: `@include layout-grid()`

### Nesting
- Maximum nesting depth: 3 levels
- Use parent selector `&` judiciously
- Flatten styles where possible

### Variables
- Use CSS custom properties for runtime values
- Use SASS variables for build-time values
- Follow naming hierarchy: `$component-element-property-state`

### Media Queries
- Use mixins for consistent breakpoints
- Mobile-first approach
- Use standard breakpoints

## Roadmap

### Phase 1: Core System
- [ ] Design tokens implementation
- [ ] Core mixins and functions
- [ ] Base reset and typography
- [ ] Utility classes

### Phase 2: Layout System
- [ ] Grid system
- [ ] Spacing utilities
- [ ] Container layouts
- [ ] Positioning helpers

### Phase 3: Component Library
- [ ] Atomic components (buttons, inputs)
- [ ] Molecular components (cards, navigation)
- [ ] Organism components (headers, footers)

### Phase 4: Theme System
- [ ] Light/dark theme support
- [ ] Custom theme creation
- [ ] Runtime theme switching

### Phase 5: Documentation
- [ ] Component usage examples
- [ ] Pattern library
- [ ] Integration guides
- [ ] Theme customization

## Contributing

Contributions are welcome! Please read our [Contributing Guide](CONTRIBUTING.md) for details on our code of conduct and the process for submitting pull requests.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.