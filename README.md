# `soft-serve` Build

> Enhanced build-only repository for [charmbracelet/soft-serve](https://github.com/charmbracelet/soft-serve) with bleeding-edge features and community patches

This repository provides pre-built versions of Soft Serve that include experimental features from upstream main branch and additional functionality from unmerged pull requests.

## ⚠️ Important Notes

- **Stability**: These builds include pre-release code that bypasses standard CI checks
- **Updates**: Follows upstream main branch closely - expect frequent changes
- **Production Use**: Recommended for testing and development environments only
- **Support**: No support here

## 🚀 Quick Start w/ Docker

```yaml
services:
  soft-serve:
    image: liuzhen932/app-soft-serve:latest
    container_name: git-app
    volumes:
      - ./data:/soft-serve
    network_mode: host
    restart: unless-stopped
```

## 🔧 What's Included

### From Upstream Main Branch

This build includes the latest commits from the official Soft Serve main branch, which may contain:

- New experimental features
- Performance improvements
- Breaking changes not yet documented
- Code that hasn't passed lint/format checks

### From Community Patches (`patches/*`)

Additional features from unmerged pull requests:

- Check the `patches/` directory for applied patches
- Each patch file includes the original PR reference
- Features are curated for stability and usefulness

## 🆚 Difference from Official Releases

| Aspect    | Official Soft Serve    | App Soft Serve             |
| --------- | ---------------------- | -------------------------- |
| Stability | Stable, CI-tested      | Experimental, pre-release  |
| Features  | Released features only | Latest + unmerged features |
| Updates   | Version releases       | Continuous from main       |
| CI Status | All checks pass        | May skip lint checks       |
| Use Case  | Production             | Testing                    |

## 🔄 Update Strategy

1. Regularly sync with upstream main branch
2. Rebase patches on top of latest upstream code
3. Release new builds
4. Test combined functionality

## 🐛 Known Issues

- Features from main branch may have incomplete implementations
- Patches may conflict with future upstream changes
- Not all combinations of patches are tested together

## 📖 Resources

- [Official Soft Serve Repository](https://github.com/charmbracelet/soft-serve)
- [Charm Bracelet](https://charm.sh/)

## 📄 License

Same license as upstream Soft Serve (MIT License). See upstream repository for details.

---

**Remember**: This is experimental software. Always backup your repositories and test in non-production environments first!
