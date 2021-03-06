Compliance Testing
==================

The goal of this test suite is to enforce the behavior an adapter must have
when implementing a functionality.  Unless a method raises NotImplementedError
an implementation MUST behave according to these tests.

Each method of the SwitchBaseOperations class MUST be Tested in this suite.

Test Format
-----------

- 1 Method = 1 Test Class
- Test classes names MUST be the tested method in CamelCase suffixed by
  "Test"
- Each test in the class MUST be by with "test_"
- Tests names SHOULD be readable by replacing "test_" with the name of the
  tested method.  Example : in a class called AddVlanTest, the test
  test_fails_if_the_vlan_exists should be read as "add_vlan fails if the
  vlan exists"

Tests Expectations
------------------

- Every client visible behavior MUST be tested and specific adapter related
  behaviors should be covered in their respective unit test suite
- Tests should be idempotent, meaning they should clean everything they added
  in a reliable way, implementing the tearDown method is reliable



