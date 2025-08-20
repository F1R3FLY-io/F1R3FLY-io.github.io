# F1R3FLY.io Documentation Portal

## Project Context
- This is the **F1R3FLY.io GitHub Pages documentation site** built with Jekyll and the Agency theme
- F1R3FLY.io specializes in **high throughput transaction servers** with a focus on distributed systems and blockchain technologies
- The organization maintains multiple projects including RNode, Rholang implementations, and hyper-dimensional computing research
- Follow F1R3FLY.io's **documentation-first development methodology** for all content and features
- If the user does not provide enough information with their prompts, ask the user to clarify before executing the task

## Site Architecture

### Technology Stack
- **Jekyll** - Static site generator for GitHub Pages
- **Agency Theme** - Bootstrap-based responsive design
- **GitHub Pages** - Automated deployment from main branch
- **Ruby/Bundler** - Dependency management for Jekyll plugins

### Content Structure
```
F1R3FLY-io.github.io/
├── _posts/           # Portfolio projects and articles
├── _includes/        # Reusable HTML components
├── _layouts/         # Page templates
├── _data/            # Site configuration data
├── img/              # Images for portfolio, team, and branding
├── css/              # Stylesheets and fonts
├── js/               # JavaScript functionality
└── index.html        # Main landing page
```

## F1R3FLY.io Organization Overview

### Core Focus Areas
- **High Throughput Transaction Servers** - Scalable distributed systems
- **Blockchain Infrastructure** - RNode platform with multi-consensus mechanisms
- **Rholang Programming Language** - Process calculus based concurrent programming
- **Hyper-Dimensional Computing** - rhoHDC encoding research
- **Developer Tools** - Language servers, parsers, and development environments

### Key Projects
1. **RNode** - Decentralized blockchain platform with four consensus mechanisms
2. **Rholang** - Concurrent programming language with formal verification
3. **rhoHDC** - Encoding of rho-calculus into hyper-dimensional computing
4. **Embers** - F1R3Sky wallets and agents
5. **Developer Tools** - Language servers, parsers, and Rust implementations

## Documentation Standards

### Documentation-First Methodology
All features and content updates must follow this process:
1. **Document Requirements** - Define purpose, audience, and acceptance criteria
2. **Create Specifications** - Technical details and implementation approach
3. **Architecture Decisions** - Document design choices and rationale
4. **Implementation** - Execute based on approved documentation
5. **Validation** - Ensure implementation matches documentation

### Documentation Structure
```
docs/
├── requirements/      # User stories, content requirements
├── specifications/    # Technical specs, SEO guidelines
├── architecture/      # Site structure, design decisions
├── api/              # Integration documentation
└── content/          # Article drafts and planning
```

### Document Naming Conventions
- **Requirements**: `REQ-*` (Requirements), `US-*` (User Stories)
- **Specifications**: `SPEC-*` (Technical), `SEO-*` (SEO/Content)
- **Architecture**: `ADR-*` (Architecture Decision Records)
- **Content**: `ARTICLE-*` (Blog posts), `PORTFOLIO-*` (Projects)

## Development Environment

### Local Development Setup
```bash
# Install Ruby and Bundler
gem install bundler

# Install dependencies
bundle install

# Serve site locally
bundle exec jekyll serve

# Build site
bundle exec jekyll build

# Watch for changes
bundle exec jekyll serve --watch
```

### GitHub Pages Deployment
- **Production**: Automatically deployed from `main` branch
- **CNAME**: Points to f1r3fly.io domain
- **SSL**: Handled by GitHub Pages

## Content Management

### Portfolio Projects
Located in `_posts/` with format: `YYYY-MM-DD-project-name.markdown`

Front matter template:
```yaml
---
layout: default
modal-id: 1
date: 2023-06-06
img: project-image.png
thumbnail: project-thumbnail.png
alt: image-alt-text
project-date: June 2023
client: Client Name
category: Development
description: Project description
---
```

### Team Members
Configured in `_config.yml` under the `people` section:
```yaml
people:
- name: Team Member
  pic: 1
  position: Role
  social:
    - title: twitter
      url: #
    - title: linkedin
      url: #
```

### Images Guidelines
- **Portfolio**: 650x350px for main, 400x289px for thumbnails
- **Team**: 225x225px square images
- **About**: 650x350px timeline images
- **Formats**: JPEG for photos, PNG for graphics with transparency

## Site Sections

### Header
- Hero image with call-to-action
- Navigation menu
- Brand positioning statement

### Services
- Core capabilities and offerings
- Technology stack highlights
- Value propositions

### Portfolio Grid
- Project showcases from `_posts/`
- Modal popups with project details
- Filterable by category

### About/Timeline
- Organization history
- Major milestones
- Technology evolution

### Team
- Core team members
- Advisory board
- Contributors

### Contact
- Contact form (requires backend setup)
- Social media links
- Physical/virtual presence

## SEO and Performance

### SEO Best Practices
- **Meta Tags**: Configure in `_config.yml` and page front matter
- **Structured Data**: Add JSON-LD for organization and articles
- **Sitemap**: Auto-generated by Jekyll
- **Alt Text**: Required for all images
- **Semantic HTML**: Use proper heading hierarchy

### Performance Optimization
- **Image Optimization**: Compress before upload
- **Minification**: CSS and JS minified in production
- **Lazy Loading**: Implement for below-fold images
- **CDN**: Leverage GitHub Pages CDN

## Common Tasks

### Adding a Portfolio Item
1. Create new post in `_posts/` with proper naming
2. Add images to `/img/portfolio/`
3. Set front matter with modal-id, images, and metadata
4. Test locally before pushing

### Updating Team Members
1. Edit `_config.yml` people section
2. Add team photo to `/img/team/`
3. Update social links
4. Rebuild site

### Modifying Site Content
1. Edit relevant include files in `_includes/`
2. Update data in `_data/template.yml`
3. Adjust styles in `/css/agency.css`
4. Test responsive design

### Creating New Sections
1. Create new include file in `_includes/`
2. Add section to `index.html`
3. Style in CSS
4. Update navigation if needed

## Testing and Validation

### Local Testing Checklist
- [ ] Links work correctly
- [ ] Images load properly
- [ ] Responsive design functions
- [ ] Forms validate (if applicable)
- [ ] SEO meta tags present
- [ ] Performance acceptable

### Browser Compatibility
- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)
- Mobile browsers

## Git Workflow

### Branching Strategy
- **main**: Production branch (auto-deploys)
- **develop**: Integration branch
- **feature/***: New features
- **fix/***: Bug fixes
- **content/***: Content updates

### Commit Guidelines
- Use descriptive commit messages
- Reference issues when applicable
- Keep commits focused and atomic
- Test before committing

### File Management
- **DO NOT** commit sensitive data
- **DO NOT** commit large unoptimized images
- **DO** use .gitignore for local files
- **DO** compress images before committing

## Security Considerations

### Best Practices
- Never commit API keys or secrets
- Use environment variables for sensitive data
- Validate all form inputs
- Keep dependencies updated
- Review third-party scripts

### Contact Form Security
- Implement CAPTCHA
- Server-side validation required
- Rate limiting recommended
- Sanitize all inputs

## Troubleshooting

### Common Issues

#### Build Failures
```bash
# Clear Jekyll cache
rm -rf _site .jekyll-cache

# Reinstall dependencies
rm Gemfile.lock
bundle install
```

#### Local Server Issues
```bash
# Kill existing Jekyll processes
pkill -f jekyll

# Use different port
bundle exec jekyll serve --port 4001
```

#### GitHub Pages Deploy Issues
- Check GitHub Pages settings
- Verify CNAME file
- Review build logs in Actions tab
- Ensure valid Jekyll configuration

## Resources

### F1R3FLY.io Links
- **Website**: [f1r3fly.io](https://f1r3fly.io)
- **GitHub**: [github.com/F1R3FLY-io](https://github.com/F1R3FLY-io)
- **Contact**: f1r3fly.ceo@gmail.com

### Documentation
- [Jekyll Documentation](https://jekyllrb.com/docs/)
- [GitHub Pages Documentation](https://docs.github.com/pages)
- [Agency Theme](https://startbootstrap.com/themes/agency/)
- [Bootstrap Documentation](https://getbootstrap.com/docs/)

## Project Principles

### Core Values
- **Documentation-First**: Every change starts with documentation
- **Transparency**: Open source and community-driven
- **Performance**: Optimize for speed and efficiency
- **Security**: Protect user data and maintain trust
- **Innovation**: Push boundaries in distributed computing

### Quality Standards
- **Code Quality**: Clean, maintainable, documented
- **Content Quality**: Accurate, engaging, valuable
- **Design Quality**: Consistent, accessible, responsive
- **Performance Quality**: Fast, efficient, scalable

## Important Instructions
- Do what has been asked; nothing more, nothing less
- NEVER create files unless absolutely necessary
- ALWAYS prefer editing existing files
- NEVER proactively create documentation files unless requested
- Follow F1R3FLY.io's documentation-first methodology
- Ask for clarification when requirements are unclear