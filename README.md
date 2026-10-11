# SauceDemo Manual Testing

Manual test suite and defect report for [saucedemo.com](https://www.saucedemo.com), a demo e-commerce site built for testing practice.

## Scope
Login, logout, and Reset App State, executed with the `problem_user` account.

## Approach
Checklist, then test cases, then execution, then bug reporting. Test cases cover positive, negative, and access-control scenarios. TC-02 uses a data table with equivalence partitioning and error guessing (empty fields, wrong credentials, leading and trailing spaces).

## Tools and environment
- Jira: test cases and bug tracking
- Confluence: test checklist
- Chrome 154 and Brave 1.97 on Windows 10

## Test cases
| ID | Title | Priority | Result |
|----|-------|----------|--------|
| TC-01 | Verify login succeeds with valid credentials | Highest | Pass |
| TC-02 | Verify that users cannot log in with invalid credentials | Highest | Pass |
| TC-03 | Verify logout works correctly | High | Pass |
| TC-04 | Verify protected pages are inaccessible after logout | High | Pass |
| TC-05 | Verify "Reset App State" clears the Cart | Low | Fail |

## Defects found
| ID | Summary | Severity | Status |
|----|---------|----------|--------|
| BUG-01 | Reset App State: product buttons still show "Remove" until page refresh | Medium | Open (To Do in Jira) |

After Reset App State, the cart badge clears but the product button keeps showing "Remove" until the page is refreshed. Also reproduced with `standard_user`.

Full report and evidence: [Bug Reports](saucedemo-manual-testing/Bug%20Reports/). Screen recording: [saucedemo - BUG -01](saucedemo-manual-testing/Bug%20Reports/saucedemo%20-%20BUG%20-01.mp4)

## Jira board
![Jira board](saucedemo-manual-testing/Screenshots/Jira%20Board.png)

## Repository contents
- [Checklist](saucedemo-manual-testing/Checklist/): test checklist
- [Test Cases](saucedemo-manual-testing/Test%20Cases/): epic overview and test cases TC-01 to TC-05
- [Bug Reports](saucedemo-manual-testing/Bug%20Reports/): BUG-01 report and evidence
- [Screenshots](saucedemo-manual-testing/Screenshots/): Jira board 
