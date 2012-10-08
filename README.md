# Things to do immediately after importing to MDN
1. Rewrite https://developer.mozilla.org/en-US/docs/Thunderbird/Thunderbird_MozMill_Testing/Running_Thunderbird_MozMill_tests_from_packaged_tests to reference built_test_packages.html#Thunderbird to reference new page on built test packages.
2. Move the following to a 'best practices' page (from https://developer.mozilla.org/en-US/docs/Creating_reftest-based_unit_tests#More_to_do)

    > There is one thing about automated tests that may not be obvious. There is really no way to construct a test that is too small. If you want to check something, and it seems trivial, that is ok. The cost of adding a new test to an automated suite is very, very low. For tests that are run manually, this is not true. The cost of thinking about and managing the execution of a manual test is fairly high. This is why manual tests tend to get longer, include more steps and ultimately become a long list that actually tests a lot of things.

    > So, create small tests. For example, it occurs to me that we assume that spaces between a element name and an attribute name have no effect, but do we know this is true? Who checks this? It is completely trivial, but so what. I can create 50 or 100 test files that have spaces between the element name and the attribute of a element for a bunch of different elements, add those to the list of tests to be run, and it causes no problems for anyone. Maybe it will actually take 500 test files to actually check this behavior. It really does not matter.

    > So, my point is, if you have an idea then create a test. Really. It would be better to have more tests than we need than too few.

3. Remove https://developer.mozilla.org/en-US/docs/Creating_reftest-based_unit_tests and/or redirect to Reftest overview.

# Things left to do in documentation overhaul
1. All the things

# Things to remove?
1. https://developer.mozilla.org/en-US/docs/Creating_reftest-based_unit_tests#Other_comparisons
2. https://developer.mozilla.org/en-US/docs/reftest_opportunities_files
3. https://developer.mozilla.org/en-US/docs/Creating_reftest-based_unit_tests#Re-building_reftest_on_Mac_OS_X

# Decision tree notes
1. Does your test require elevated privileges?
   * Yes: Mochitest, Mozmill
   * No: Reftest
