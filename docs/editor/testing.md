---
Order: 8
Area: editor
TOCTitle: Testing
ContentId: d44f1a5c-5454-4037-92d5-c2bf5d4cffed
PageTitle: Testing in Visual Studio Code
DateApproved: 05/02/2024
MetaDescription: One of the great things in Visual Studio Code is testing support. Automatically discover tests in your project, run and debug your tests, and get test coverage results.
---
# Testing

Software testing is a crucial aspect of the software development process. It helps ensure that your code works as expected and catches bugs early in the development cycle. Visual Studio Code provides a rich set of features for testing your code. You can automatically discover tests in your project, run and debug your tests, and get test coverage results.

In this article, you'll learn how to get started with testing in VS Code, discover popular testing extensions, and explore the testing capabilities.

![Testing in Visual Studio Code](images/testing/testing-hero.png)

## Getting started with testing in VS Code

Testing support in VS Code is language-specific and depends on the [extensions](#testing-extensions) you have installed. The testing features are provided by the language extensions, which can be language servers, test runners, or other tools that support testing in that language. To get started with testing in VS Code, first install the appropriate language extension for your project.

Once you have the language extension installed, you can start discovering and running tests in your project. The [Test Explorer](#automatic-test-discovery-in-test-explorer) provides a centralized place to manage and run your tests.

After you run your tests, you can view the test results in the Test Explorer view, editor gutter, and Test Results panel. To diagnose issues with your tests, you can also [run and debug tests](#run-and-debug-tests) and set breakpoints in your test and application code.

You can also [run tests with coverage](#test-coverage) to see how much of your code is covered by your tests. Test coverage helps you identify areas of your code that are not being tested and ensures that your tests are comprehensive. You can view the test coverage results in different views in the editor and Test Coverage panel.

To optimize your testing workflow, you can [create tasks to run your tests](#task-integration), and optionally run your tests in the background with every code change.

## Testing extensions

You can find extensions that support testing by looking in the [Visual Studio Marketplace](https://marketplace.visualstudio.com/search?target=VSCode&category=Testing&sortBy=Installs). You can also go to the Extensions view (`kb(workbench.view.extensions)`), and filter by the **Testing** category. You can then sort by **Install count** or ratings to see which extensions are popular.

<!-- <div class="marketplace-extensions-testing"></div> -->

> **Tip**: The extensions shown above are dynamically queried. Select an extension tile to read the description and reviews to decide which extension is best for you.

## Automatic test discovery in Test Explorer

The Test Explorer view provides a centralized place to manage and run your tests. You can access the Test Explorer view by selecting the beaker icon in the Activity Bar or by using the **Testing: Focus on Test Explorer View** command in the Command Palette (`kb(workbench.action.showCommands)`).

If you have a project with tests, the Test Explorer view automatically discovers and lists the tests in your workspace. By default, the discovered tests are displayed in a tree view in the Test Explorer. The tree view matches the hierarchical structure of your tests, making it easy to navigate and run your tests.

![Test Explorer view](images/testing/test-explorer-view.png)

You can run tests from the Test Explorer by selecting the play button. Learn more about running and debugging tests in the [Run and debug tests](#run-and-debug-tests) section.

The tree view shows the test result status for each test by using a visual indicator, and enables you to run and debug tests, and navigate to the test code.

![Test Explorer view with test results](images/testing/test-explorer-view-test-results.png)

> **Tip**: You can navigate to the test code by double-clicking on the test in the Test Explorer view. If you select a test that failed, the editor opens the test file, highlights the failed test, and shows the error message.

If you have many tests, you can use the filtering options to quickly find the tests you're interested in. You can use the **Filter** button to filter tests by status or only show tests for the current file. You can also use the search box to search for specific tests by name or use the `@` symbol to search by status.

![Test Explorer view with filtering options](images/testing/test-explorer-view-filtering.png)

In the **More Actions** menu, you can access additional functionality, such as sort and display options.

If you add new tests or make changes to your tests, use the **Refresh Tests** button to refresh the list of tests in the Test Explorer. You can also use the **Test Explorer: Reload tests** command in the Command Palette (`kb(workbench.action.showCommands)`).

## Run and debug tests

After the discovery of the tests in your project, you can run and debug your tests, and view test results directly from within VS Code. You have multiple options to run and debug tests:

- Use the actions in the Test Explorer view to run all or a subset of tests
- Use the controls in the editor gutter to run tests while you're editing your test code
- Use the commands to run tests from the Command Palette (`kb(workbench.action.showCommands)`)

In the Test Explorer, use the controls in the section heading to run or debug all tests. You can also run or debug individual tests by selecting the play or debug icon next to the test name. In the tree view, when you select to run or debug on a specific node, all tests under that node are run or debugged.

![Run and debug tests in Test Explorer](images/testing/run-debug-tests-test-explorer.png)

While you're viewing your test code in the editor, you can use the play control in the gutter to run the test at the current cursor position. Right-click on the gutter control to view other actions, such as debugging the test.

![Run and debug tests in editor gutter](images/testing/run-debug-tests-editor-gutter.png)

> **Tip**: you can configure the default testing action for the gutter control by using the `testing.defaultGutterClickAction` setting.

After running a test, the editor gutter displays the test status.

When you run tests, the test result status is displayed in the Test Explorer view and editor gutter. The test results are color-coded to indicate the status of the test (pass or fail). When a test fails, notice that the test error message is shown as an overlay in the editor.

Use the **Show Output** button in the Test Explorer to view the test output in the **Test Results** panel.

![Test Results panel](images/testing/test-results-panel.png)

You can access the commands for the Test Explorer, such as running or debugging tests, via the Command Palette (`kb(workbench.action.showCommands)`). Enter `Test Explorer:` to find the corresponding commands.

## Test coverage

- Run tests with coverage
- Test Coverage panel
- View coverage in editor
- View coverage in Explorer view
- Also shown in diff editor

## Task integration

- Create task to run tests (Test: Run test), optionally create keyboard shortcut
- Configure to run in background

Learn more about [using and configuring Tasks](/docs/editor/tasks.md).

## Test configuration settings

- Configure `testing.xxx` for general testing settings
- Add table of settings

## Next steps

- Get started with testing in Python, Java, C#