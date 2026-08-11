```markdown
# Telegraph-Image Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill teaches you the core development patterns and workflows used in the Telegraph-Image JavaScript codebase. You'll learn the project's coding conventions, how to add features, fix bugs, update documentation (in both English and Chinese), and maintain test coverage. The repository is framework-agnostic, using plain JavaScript with a focus on modular backend functions and a simple admin UI.

## Coding Conventions

- **File Naming:**  
  Use `camelCase` for file and folder names.  
  _Example:_  
  ```
  functions/upload.js
  functions/file/getImage.js
  ```

- **Import Style:**  
  Use relative imports for modules within the project.  
  _Example:_  
  ```js
  const { resizeImage } = require('../utils/imageUtils');
  ```

- **Export Style:**  
  Use named exports for functions and objects.  
  _Example:_  
  ```js
  // In functions/utils/imageUtils.js
  function resizeImage(img, size) { /* ... */ }
  module.exports = { resizeImage };
  ```

- **Commit Messages:**  
  Use prefixes like `feat`, `fix`, or `docs` to indicate the type of change.  
  _Example:_  
  ```
  feat: add image compression to upload endpoint
  fix: correct MIME type handling in file proxy
  docs: update usage instructions in README
  ```

## Workflows

### Feature Development with Tests and Docs
**Trigger:** When adding a new feature or significant enhancement  
**Command:** `/new-feature`

1. Implement backend logic in the appropriate function file(s), e.g., `functions/upload.js` or `functions/file/[id].js`.
2. Update or add utility/helper modules if needed, e.g., `functions/utils/imageUtils.js`.
3. Update admin UI files (`admin.html`, `admin-imgtc.html`) to reflect new or changed features.
4. Add or update automated tests in `test/*.test.js` or `test/helpers.js`.
5. Update documentation in both `README.md` and `README-zh.md` to describe the new feature.

_Example:_
```js
// functions/upload.js
function uploadImage(req, res) {
  // New feature logic here
}
module.exports = { uploadImage };
```

### Documentation Update (Dual Language)
**Trigger:** When updating documentation for new features or onboarding materials  
**Command:** `/update-docs`

1. Edit `README.md` to add or update documentation.
2. Edit `README-zh.md` to mirror changes in Chinese.
3. Ensure both files are in sync in terms of structure and content.

_Example:_
```
# README.md
## New Feature
Description and usage...

# README-zh.md
## 新功能
描述和用法...
```

### Backend Bugfix with Test
**Trigger:** When fixing a bug in backend logic  
**Command:** `/fix-bug`

1. Fix the bug in the relevant backend function file, e.g., `functions/file/[id].js`.
2. Add or update a test file to cover the fixed behavior, e.g., `test/file-proxy.test.js`.

_Example:_
```js
// functions/file/getImage.js
function getImage(req, res) {
  // Bugfix applied here
}
module.exports = { getImage };

// test/file-proxy.test.js
const { getImage } = require('../functions/file/getImage');
test('should return correct MIME type', () => {
  // Test logic here
});
```

## Testing Patterns

- **Test Files:**  
  Located in the `test/` directory, named with the `.test.js` suffix.
- **Test Framework:**  
  Not explicitly specified; tests are written in plain JavaScript or using a lightweight test runner.
- **Helpers:**  
  Common test utilities are placed in `test/helpers.js`.
- **Example Test File:**
  ```js
  // test/upload.test.js
  const { uploadImage } = require('../functions/upload');
  test('uploads image successfully', () => {
    // Test logic
  });
  ```

## Commands

| Command        | Purpose                                                      |
|----------------|--------------------------------------------------------------|
| /new-feature   | Start a new feature with backend, UI, tests, and docs        |
| /update-docs   | Update documentation in both English and Chinese             |
| /fix-bug       | Fix a backend bug and add/update a corresponding test        |
```
