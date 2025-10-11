https://github.com/Lakshya234/tutorial-react-native-expo-2sem-2025/releases

# Tutorial React Native with Expo: Build iOS & Android Apps

[![Releases](https://img.shields.io/badge/releases-visit%20releases-blue?style=for-the-badge)](https://github.com/Lakshya234/tutorial-react-native-expo-2sem-2025/releases)  
[![Repo Type](https://img.shields.io/badge/tech-React%20Native%20%26%20Expo-blueviolet?style=for-the-badge)](https://reactnative.dev/)  
[![License](https://img.shields.io/badge/license-MIT-brightgreen?style=for-the-badge)](LICENSE)

Welcome to the repository for a practical guide to building mobile apps with React Native and Expo. This project focuses on teaching you how to create cross‑platform apps for iOS and Android, using Expo as the build and development workflow. It is written in a straightforward, hands‑on manner to help you grasp core concepts quickly and apply them in real projects.

Overview
- Project aim: Provide a clear, practical path to creating mobile apps with React Native and Expo, covering setup, core components, navigation, data handling, and deployment basics.
- Target audience: Students, developers in a boot camp, or anyone who wants a structured, hands‑on introduction to React Native with Expo.
- Language: Portuguese, with code comments and explanations in plain English where helpful for cross‑reference.
- Repository name: tutorial-react-native-expo-2sem-2025
- Repository info: Tutorial React Native com Expo - Criando Apps para iOS e Android
- Topics: not provided

This guide uses a methodical, no‑nonsense approach. You will learn by doing: you will spin up a local project, build screens, connect to a simple API, and run the app on simulators or real devices. The goal is to make you confident in setting up a project, choosing the right patterns, and understanding the Expo workflow.

Table of contents
- Why use React Native with Expo?
- Quick start: prerequisites
- Getting the project up and running
- Project structure explained
- Core concepts you will learn
- Building user interfaces
- Navigation and flows
- Data handling and state management
- Networking and API integration
- Persistent storage and offline capabilities
- Local and remote assets
- Theming, accessibility, and performance
- Testing and debugging
- Release process and distribution
- Development workflow and best practices
- Contributing and contributing guidelines
- Licensing and attribution
- Appendix: common questions and troubleshooting

Why use React Native with Expo?
- Cross‑platform development: Write once, run on both iOS and Android.
- Rapid iteration: Expo provides a fast workflow for development, testing, and sharing.
- Ready‑to‑use components: A rich set of UI primitives designed for mobile experiences.
- Strong ecosystem: A large community and a robust set of plugins and libraries.
- Accessible tooling: Expo Go lets you test quickly on real devices, while building for stores is streamlined with EAS Build.

Getting started: prerequisites
Before you start building, you need a few essential tools. This section keeps things simple and actionable, so you can begin quickly even if you are new to mobile development.

Hardware and environment
- A computer with macOS, Windows, or Linux.
- An internet connection with stable bandwidth for downloading dependencies and assets.
- Access to an iPhone or Android device for live testing, or an emulator/simulator on your computer.

Software prerequisites
- Node.js (v14 or newer). You should avoid using older LTS releases for new projects. Node includes npm, which you can use to install packages.
- npm or Yarn as a package manager. npm comes with Node by default; Yarn is optional if you prefer it.
- Expo CLI (global) for mobile development workflows. You can install it with npm install -g expo-cli.
- Watchman (optional, macOS) to improve performance on file watching.
- Android Studio (for Android emulation) or Xcode (for iOS emulation on macOS) if you plan to test on simulators.
- A code editor you like (Visual Studio Code is a popular choice due to its integrated terminal, intellisense, and extensions for React Native).
- A Git client for version control if you want to contribute or keep code history.

Installation basics
- Install Node.js from the official site. This will also install npm.
- Install Expo CLI globally: npm install -g expo-cli
- Install the chosen package manager (npm comes bundled with Node.js; yarn is optional).
- If you work on macOS, install Watchman for better file watching.
- Install Android Studio and/or Xcode if you want to run emulators locally. Ensure you configure the Android SDK path and Xcode command line tools.

Getting the project up and running
This repository provides a practical path to get a React Native with Expo project up and running. The process has two primary tracks: running the project locally on your machine and using the release asset for a prebuilt setup.

Important note about the release asset
- The Releases page contains downloadable assets that represent a snapshot of the project. If you are using the provided link, you should download the release asset and execute it according to the instructions in the asset's README or installer description. The Release page is the fastest way to see a ready‑to‑run version of the project for hands‑on exploration.

From the Releases page, you will typically find a prebuilt app bundle, a demo installation, or a zipped project folder that you can extract and run. If you are unsure which asset to pick, choose the one labeled for Expo or the one described as a runnable demo. After downloading, follow the included instructions to install or run the app.

For those who prefer to work from source, you can clone this repository and run the project locally. The steps below cover both options.

Quickstart: run the project locally
1) Clone the repository (optional)
- If you want to work with the source, clone this repository to your local machine:
  - git clone https://github.com/Lakshya234/tutorial-react-native-expo-2sem-2025.git
- Navigate into the project directory:
  - cd tutorial-react-native-expo-2sem-2025

2) Install dependencies
- Open a terminal in the project root and install dependencies:
  - npm install
- If you prefer Yarn:
  - yarn install

3) Start the Expo development server
- Start the project with Expo:
  - npx expo start
- This launches the Metro bundler and shows a QR code you can scan with the Expo Go app on iOS or Android.

4) Run on devices or simulators
- iOS: Scan the QR code with the Expo Go app on an iPhone. If you have Xcode installed, you can also run on the iOS simulator from the Expo Dev Tools.
- Android: Scan the QR code with the Expo Go app on an Android device. You can also start an Android emulator from Android Studio and connect to the dev server.

5) Common commands you will use
- Start the dev server without opening a browser:
  - npx expo start --no-dev-client
- Build a standalone app for testing or production:
  - expo build:android or expo build:ios (for legacy builds) or use EAS Build for modern workflows.
- Run tests (if you add tests later):
  - npm test or yarn test

Notes about running the release asset
- If you download the prebuilt release asset, you may need to unzip or extract the package, then run the appropriate installer or app. Follow the included README inside the asset, as instructions may vary between assets. The asset might be an APK for Android, an IPA for iOS (on devices with proper provisioning), or a bundle you can load with Expo Go.

Project structure explained
A clear project structure helps you navigate quickly and avoid confusion. Here is a representative layout you will see in this repository. The exact names may vary slightly, but the intent remains consistent.

- App.tsx or App.js
  The entry point of the app. It wires up navigation, providers, and the top-level screens.

- src/
  A common place to store application code. The src directory often contains:
  - components/
    Reusable UI elements such as buttons, cards, form controls, and layout primitives.
  - screens/ or views/
    Each screen or major view of the app, such as Home, Details, Settings, and Profile.
  - navigation/
    Stack, tab, and drawer navigators. This directory holds the navigation logic that moves users through the app.
  - features/ or modules/
    Groupings for larger features. Each feature contains components, hooks, and sometimes its own navigation.
  - services/ or api/
    Data fetching, API clients, and network utilities.
  - hooks/
    Custom React hooks for shared logic like data fetching, debouncing, or state synchronization.
  - store/ or state/
    State management logic, reducers, actions, and store configuration (e.g., Redux or context providers).
  - assets/
    Images, icons, fonts, and other static assets.
  - config/
    Environment variables, API base URLs, and feature flags.
  - types/ or interfaces/
    Type definitions for TypeScript projects.

- android/ and ios/
  Native project files for Android and iOS builds. Expo can manage these for you with EAS Build, but you may still see native directories if you eject or work with bare workflows.

- README.md
  The file you are reading now. It provides guidance, usage, and conventions for the project.

- package.json
  The manifest for the project. It lists dependencies, scripts, and metadata about the project.

- tsconfig.json
  TypeScript configuration (if the project uses TypeScript).

- .gitignore
  Specifies files and directories that should not be tracked by Git.

Core concepts you will learn
- React Native basics: components, props, state, hooks, and styling.
- Expo workflow: an all‑in‑one toolchain for building, deploying, and debugging.
- Navigation: moving between screens with stack and tab navigators.
- Layouts: flexbox, alignment, spacing, and responsive design for different screen sizes.
- Theming: light and dark mode themes, color tokens, and accessible contrast.
- Data flow: local state, lifting state, and simple global state strategies.
- Networking: calling REST APIs, handling responses, and error states.
- Storage: lightweight persistence for user preferences or offline data.
- Accessibility: making apps usable by a broad audience, including keyboard navigation and screen‑reader support.
- Performance: optimizing renders, using memoization, and reducing re-renders.
- Testing basics: unit ideas, basic UI tests conceptually, and practical debugging steps.
- Release and distribution: understanding how to prepare apps for stores or test deployments.

Building user interfaces
- Design system approach: use a consistent set of tokens for colors, typography, spacing, and elevation.
- Components: create small, reusable components that can be composed into screens.
- Styles: prefer inline styles or StyleSheet.create for performance. Keep styles modular and predictable.
- Accessibility: add accessibilityLabels and roles where appropriate; ensure color contrast is good; provide scalable text support.

Navigation and flows
- Stack navigation: typical for screen-to-screen flows in a mobile app.
- Tab navigation: bottom tabs for primary app sections.
- Drawer navigation: side menus for secondary options.
- Deep linking: enabling navigation via URLs for better marketing and sharing routes.

Data handling and state management
- Local state: use useState and useReducer for simple cases.
- Shared state: use React Context for lightweight global state.
- Persisted state: store user preferences or recently viewed items in AsyncStorage or a simple file-based approach.
- Network state handling: show loading indicators, handle errors gracefully, and present retry options.

Networking and API integration
- Base URL management: centralize the API base URL in a config file.
- Fetch patterns: use fetch or axios; handle JSON conversion and error cases.
- Error handling: present user-friendly messages for network failures and server errors.
- Security: avoid exposing API keys in front‑end code; use environment configurations for different environments.

Persistent storage and offline capabilities
- AsyncStorage or community alternatives: store small bits of data locally.
- Caching strategies: cache API results to speed up the UI and reduce network calls.
- Offline mode: provide a graceful fallback when the network is unavailable.

Local and remote assets
- Local assets: images and fonts included in the app bundle for fast loading.
- Remote assets: load images from the network; handle slow connections with placeholders and progressive loading.
- Font loading: load custom fonts to improve typography and brand alignment.

Theming, accessibility, and performance
- Theming: support light and dark themes; use a centralized color system.
- Accessibility: semantic roles, accessible labels, and touch targets that meet recommended sizes.
- Performance: avoid heavy re-renders; optimize images; memoize expensive components; use lazy loading where appropriate.

Testing and debugging
- Quick checks: run the app on multiple devices to catch platform-specific issues.
- Debugging: use React DevTools, React Native Debugger, and Expo DevTools to inspect component trees and network activity.
- Logging: implement a simple logging strategy; avoid noisy console output in production.

Release process and distribution
- Release management: track changes via conventional commits; tag releases; maintain a changelog.
- Building for stores: use Expo EAS Build for robust build pipelines; configure the necessary credentials and environment settings.
- Distribution: publish beta builds to services like TestFlight and Google Play Console; provide testers with access instructions.
- Documentation: maintain a concise release note in the Releases section describing what changed, what to test, and any migration notes.

Development workflow and best practices
- Branching strategy: use a simple feature branch approach (feature/your-feature) and a main branch for stable releases.
- Code quality: run linting and type checking; use pre-commit hooks to enforce standards.
- Documentation: keep inline comments useful and up to date; document any non-trivial decisions.
- Dependency management: prefer semantic version ranges and pin exact versions only when necessary.
- Security: avoid hard‑coding credentials; use environment variables and secure storage for secrets.

Contributing and contributing guidelines
- How to contribute: fork the repository, create a feature branch, implement your changes, and submit a pull request.
- Code style: follow the conventions used in the project; keep functions small and focused.
- Testing: include tests where feasible; describe manual tests you performed.
- Issues: search open issues to avoid duplicating work; reference issues in your PRs.
- Community standards: be respectful, concise, and constructive in discussions.

Licensing and attribution
- This project uses the MIT license. You are free to use, modify, and distribute the code with minimal restrictions.
- Attribution: credit the original authors when reusing code or assets in your own projects.
- Third‑party libraries: many dependences come with their own licenses; review them if you plan to reuse parts of the code.

Appendix: troubleshooting and common questions
- Why does the app not start after a fresh install?
  - Ensure you have a supported Node.js version.
  - Check that dependencies were installed correctly.
  - Verify that the Expo server is running and that your device can reach it.
  - Look at the logs for error messages pointing to missing assets or permissions.

- How do I run on a real device?
  - Install Expo Go on your device.
  - Start the project with npx expo start.
  - Scan the QR code with the camera to open the app in Expo Go.
  - If you want to build a standalone app, use Expo’s build or EAS Build workflow.

- What if I face iOS simulator issues?
  - Make sure Xcode command line tools are installed and up to date.
  - Start the iOS simulator from Xcode or from Expo DevTools.
  - Ensure you have the correct iOS simulator device selected.

- How do I test API calls?
  - Use a mock server during development to avoid hitting live endpoints.
  - Validate error handling for network failures and API errors.
  - Log responses in a way that helps you diagnose mismatched data formats.

- How to handle environment-specific configurations?
  - Use a dedicated configuration file or environment variables for each environment (development, staging, production).
  - Suppress sensitive data in logs; never commit secrets to version control.
  - Provide a clean switch in the app to adjust endpoints and feature flags without redeploying.

- How to update dependencies safely?
  - Use a package manager with lock files (npm or Yarn) to ensure determinism.
  - Update one dependency at a time and test thoroughly.
  - Run linting and tests after each dependency update to catch breaking changes early.

- How to contribute a new feature?
  - Propose a feature in an issue or discussion thread first.
  - Create a feature branch with a descriptive name.
  - Implement the feature with tests where possible.
  - Document the feature in the README or dedicated docs.
  - Submit a pull request and engage in the review process.

- How to handle accessibility concerns?
  - Ensure tappable elements meet minimum target sizes.
  - Provide alt text for images and descriptive names for UI controls.
  - Use semantic components where possible and expose proper accessibility labels.
  - Test keyboard navigation for critical flows.

- How to approach performance improvement?
  - Profile the app to identify slow components.
  - Use memoization and lazy loading for heavy components or screens.
  - Optimize image sizes and use progressive image loading.
  - Minimize re-renders by stabilizing props and using stable callbacks.

- How to customize themes and branding?
  - Centralize color tokens and typography in a theme file.
  - Expose a theme switcher to adapt to light/dark modes.
  - Update icons and imagery to align with your brand identity.
  - Check contrast ratios and ensure readability in all themes.

- How to handle data persistence?
  - Choose a storage strategy that fits the data's size and usage pattern.
  - Sync critical data to a remote backend when online.
  - Provide a fallback path for offline users, including a graceful error state when data is unavailable.

- How do we ensure code quality?
  - Use static analysis tools to catch issues early.
  - Write unit tests for critical logic and integration tests for workflow flows.
  - Maintain consistent formatting with a shared style guide.
  - Keep dependencies lean and maintain an up‑to‑date security posture.

- How to publish a new release?
  - Prepare release notes describing what changed, what users need to test, and any migration notes.
  - Increment the version number following semantic versioning rules.
  - Build the app for the target platforms using Expo EAS or an alternative workflow.
  - Tag the release in Git and push the artifacts to the Releases page.
  - Communicate the release to testers and users with clear instructions.

- How to roll back or revert changes?
  - Use Git to revert a commit or revert a feature branch to a previous state.
  - Rebuild and retest after rollback to ensure compatibility with the rest of the codebase.
  - Update release notes to reflect the rollback and any user actions required.

- How to handle cross‑platform issues?
  - Maintain a checklist to verify UI parity across iOS and Android.
  - Use platform‑specific code paths only when necessary.
  - Test on both platforms frequently during development.
  - Document any platform expectations in the code comments and in the docs.

- How to work with assets responsibly?
  - Keep asset sizes reasonable to reduce app load times.
  - Use vector assets where possible for scalability.
  - Provide appropriate fallback images for low‑bandwidth environments.
  - Cache assets to minimize repeated downloads and improve performance.

- How to integrate with external services?
  - Implement a clean service layer to abstract API calls.
  - Handle authentication securely and refresh tokens when needed.
  - Log request outcomes and provide user‑friendly error messages.
  - Respect rate limits and implement backoff strategies.

- How to manage localization and accessibility for multiple languages?
  - Use a localization library to manage strings in different languages.
  - Externalize all user‑facing text to translation files.
  - Provide right‑to‑left (RTL) support if needed.
  - Ensure UI adapts to language length differences to prevent layout breakage.

- How to document your work effectively?
  - Keep a clear, up‑to‑date README with setup steps, usage, and examples.
  - Add inline code comments where logic might be unclear.
  - Create a small developer guide for contributors covering coding standards.
  - Maintain a changelog that tracks changes across releases.

- How to keep the project organized as it grows?
  - Use feature folders to group related components, screens, and utils.
  - Maintain a consistent naming convention for files and components.
  - Document the intended use of each module to guide future contributors.
  - Regularly prune unused dependencies and visit the licensing terms.

- How to handle security considerations?
  - Avoid exposing secrets in the codebase.
  - Use secure storage for sensitive information and credentials.
  - Regularly audit dependencies for vulnerabilities.
  - Implement proper error handling to avoid leaking stack traces or sensitive data.

- How to plan for future enhancements?
  - Maintain a backlog with prioritized user stories.
  - Plan sprints or iteration cycles to deliver value consistently.
  - Create a lightweight architecture that can evolve as the app grows.
  - Schedule periodic refactoring to keep the codebase maintainable.

- How to learn more and stay up to date?
  - Follow React Native and Expo release notes to track changes and new features.
  - Explore examples and sample projects to see patterns in action.
  - Experiment with new libraries and tools in a dedicated branch before merging to main.
  - Join community forums, Discord or Slack channels to share knowledge and ask questions.

Appendix: sample technical decisions
- State management choice: For this tutorial, we favor a small, scalable approach. We start with React Context for simple global state and a few custom hooks to keep logic encapsulated. If the app grows, we can introduce a lightweight store like Zustand or a Redux pattern adapted to the scope of the project.
- Navigation strategy: A combination of stack navigation for flows and bottom tab navigation for primary sections. This mirrors common mobile app design patterns and provides a natural user experience.
- API integration approach: A plain REST API client, with a central service wrapper to handle base URLs, headers, and common error handling. Errors are surfaced to the UI with user‑friendly messages and retry options.

Images and visuals
- App previews: Include screenshots of the app in different contexts (home screen, detail view, form, and settings). These visuals help readers understand the UI layout and design approach.
- Logos and branding: Use recognizable logos from the React Native and Expo ecosystems to illustrate the toolchain. Include a branding guide in the project if you establish a design system.
- Icons: Use consistent icons from a reputable icon set to convey actions (save, delete, edit, navigate) and states (loading, success, error).
- External images: If you embed images from external sources, make sure you have permission to reuse them and credit the sources where appropriate. When possible, host assets within the repo under assets/ for stability.

Screenshots and demos
- Provide several end‑to‑end screenshots or animated GIFs showing the app in action. Include captions that explain what the user is seeing in each image.
- For a deeper understanding, add a short walkthrough video demonstrating the primary user flows (e.g., onboarding, login, item creation, list filtering, profile updates). If hosting a video within the repository is feasible, include a link to the video in this README and provide a descriptive alternative text for accessibility.

Accessibility and inclusive design
- Focus on readable typography with adequate line height and font size.
- Ensure color contrast meets accessibility standards. Provide high‑contrast themes and test with a color contrast analyzer.
- Support screen readers by using accessible labels and semantic components where possible.
- Include scalable UI that adapts to different screen sizes and orientations.

Localization and internationalization
- Start with a single language (Portuguese, given the repository context) and plan for adding other languages as the project grows.
- Externalize text into translation files, and use a localization library to switch languages at runtime.
- Test the app with different languages to identify layout issues caused by longer or shorter phrases.

Development notes and guidelines
- Keep code modular: break complex components into smaller, reusable parts.
- Document decisions: add comments that explain why a particular approach was chosen, not just what the code does.
- Keep dependencies minimal and purposeful. Remove unused packages to avoid bloat.
- Use a consistent commit message format to improve traceability.
- Ensure the project builds cleanly in both development and production modes.

Release notes and changelog
- Maintain a changelog that records user‑visible changes, bug fixes, performance improvements, and any breaking changes.
- Align release notes with the semantic versioning approach. Note the version in the tag and the associated changelog section.
- For each release, provide quick steps to reproduce or test the changes, plus any migration notes if applicable.

Contributing and social aspects
- Encourage new contributors to open issues before coding to discuss scope.
- Provide a simple contribution guide with steps to fork, branch, commit, test, and submit a pull request.
- Welcome feedback from learners and developers with different backgrounds. Strive to create inclusive, beginner‑friendly content.
- Document how to set up a local development environment, how to run the app, and how to test changes before submitting a PR.

Documentation and sources
- This repository serves as a practical tutor, not just a theory base. It blends conceptual explanations with hands‑on tasks that reinforce learning by doing.
- Use inline code examples to illustrate common tasks, such as navigating between screens, fetching data, or handling form input.
- When introducing new libraries or APIs, provide a brief rationale for their use and point to official documentation for readers who want to dive deeper.

License and attribution
- The project is released under the MIT license, which allows broad use with minimal constraints. Include any attribution required by third‑party libraries you include in the project.
- Where possible, reference official documentation and tutorials that informed the approach, so readers can explore further.

Cleanup and maintenance tips
- Regularly review dependencies for security or performance issues. Update them in small, testable steps.
- Refactor frequently touched parts of the code to keep it maintainable as new features land.
- Add or update tests for critical features as the project grows.

Closing notes
- This README is designed to be a practical companion for learners and contributors. It emphasizes hands‑on learning, clarity, and a calm, methodical workflow.
- As you iterate on the project, keep the structure coherent, the naming consistent, and the documentation up to date. Clear guidance helps new learners and seasoned developers alike.

Releases and the knowledge you gain
- The Releases page is a living repository of the project’s progress. If you are exploring this project in a classroom or self‑paced learning scenario, the latest release often contains a runnable demo you can inspect and experiment with offline. To access it, visit the link below and pick the asset that fits your setup. The asset may be an APK, a ZIP archive, or a prebuilt bundle ready for Expo Go. Following the asset’s instructions will help you understand how the project looks and works in a near‑production environment.

- For more context and the latest updates, you can repeatedly refer to the Releases page. It serves as a succinct snapshot of what has changed since the previous release and what to verify in your own environment.

- If you are new to this repository, the Releases section is a good starting point. It provides a concrete example you can run to see how the app behaves. You can compare your local build with the released one to identify differences and learn how small changes affect the user experience.

Additional resources
- Official React Native documentation: foundational concepts, API references, and migration guides.
- Expo documentation: detailed guides on the Expo SDK, expo‑go, EAS Build, and deployment workflows.
- TypeScript (if used): types, interfaces, and best practices for defining data structures in React Native.
- Accessibility resources: best practices for making mobile apps accessible to a wide range of users.
- Security and privacy guidelines for mobile apps: data handling, encryption, and secure storage considerations.

Project milestones (illustrative)
- Milestone 1: Project scaffolding, navigation skeleton, and a simple home screen.
- Milestone 2: Form input, validation, and a detail page with data binding.
- Milestone 3: API integration with a mock server and offline handling for basic data persistence.
- Milestone 4: Theming, localization scaffold, and accessibility improvements.
- Milestone 5: Performance tuning, basic tests, and a release candidate.
- Milestone 6: Final polish, documentation, and a final release that demonstrates the end‑to‑end workflow.

Notes on this README’s style and approach
- The content emphasizes clarity, direct instructions, and practical steps.
- It keeps sentences short and focused, favoring the active voice.
- It uses plain language, avoiding unnecessary jargon where possible, but it includes relevant technical terms to help readers understand the concepts.
- It maintains an approachable tone that conveys calm confidence about building mobile apps with Expo.

Reiterating the release link
- Access the release assets here: https://github.com/Lakshya234/tutorial-react-native-expo-2sem-2025/releases
- The asset in the Releases page should be downloaded and executed according to the included instructions. If you need to review the latest package before running it, head back to the Releases page. The asset will guide you through the exact steps to experience the project on your device or emulator.

End of document

