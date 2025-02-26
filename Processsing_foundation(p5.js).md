# p5.js: A Friendly Tool for Learning to Code and Create Art

p5.js is an open-source JavaScript library designed for creative coding, allowing users to learn programming while making art. It's free to use and accessible for beginners, designers, and artists alike.

- **Main repository:** [p5.js GitHub](https://github.com/processing/p5.js/)
- **Community forum:** [Processing Forum - Summer of Code](https://discourse.processing.org/c/summer-of-code/26)
- **Discord server:** [p5.js Discord](https://discord.com/channels/836700474425475088/)

---

## Quick Start Guide for Developers

If you're looking to contribute to the p5.js codebase — whether to improve p5.js itself or its sub-projects like the Friendly Error System — follow these steps:

1. **Fork the p5.js repository**  
   Create a fork of the p5.js repository on GitHub.

2. **Clone your fork to your local machine**  
   Clone your personal fork to work on your local computer.

3. **Add the upstream repository**  
   Add the original p5.js repository as an upstream remote to keep your fork up to date:
   ```bash
   git remote add upstream https://github.com/processing/p5.js
   ```

4. **Ensure Node.js is installed**  
   Check that Node.js is installed on your machine with the following command:
   ```bash
   node -v
   ```

5. **Install dependencies**  
   Install all necessary dependencies by running:
   ```bash
   npm ci
   ```

6. **Create a new git branch**  
   Create a new branch based on the main branch, giving it a descriptive name:
   ```bash
   git checkout -b [branch_name]
   ```

7. **Run tests frequently**  
   As you make changes, it's important to frequently run tests to ensure you're not breaking existing functionality. Run tests with:
   ```bash
   npm test
   ```

8. **Add unit tests (if applicable)**  
   If you're adding new features or enhancing existing ones, be sure to add relevant unit tests.

9. **Commit your changes and submit a Pull Request**  
   Once you've completed your changes, commit them and open a pull request to contribute your work back to the main repository.
