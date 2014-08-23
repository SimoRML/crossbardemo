**WAMP Testcases**
____________

# 3 Remote Procedure Calls

## 3.1 Argument and return types (Number)


### 3.1.1 Scalar Value Echo (Number)

*Description*

Echo a single scalar value of number type.

*Expectation*

The value is roundtripped exactly.

*Signature*

     (value|number) -> result|number

     value:   The value to be echo'ed back.
     result:  The echo'ed value.

Each of the following endpoints is tested with all test values from below.

#### Tested Endpoints

 * `http://api.testsuite.wamp.ws/case/3.1.1#1`
 * `http://api.testsuite.wamp.ws/case/3.1.1#2`
 * `http://api.testsuite.wamp.ws/case/3.1.1#3`
 * `http://api.testsuite.wamp.ws/case/3.1.1#4`

#### Tested Values

Zero as value:

       0

Each value from the following series of positive integers:

       [2^7-1, 2^8-1, 2^15-1, 2^16-1, 2^31-1, 2^32-1, 2^63-1, 2^64-1]

Each value from the following series of negative integers:

       [-2^7, -2^15, -2^31, -2^63]

Each of the following floating point numbers:

       [0, 0.1, 0.125, 0.2, ... FIXME]


### 3.1.2 Add Two Numbers

*Description*

Add two values of number type.

*Expectation*

The sum of both values is returned.

*Signature*

     (value1|number, value2|number) -> result|number

     value1:  The first value to be added.
     value2:  The second value to be added.
     result:  The sum of value1 and value2.

Each of the following endpoints is tested with all test values from below.

#### Tested Endpoints

 * `http://api.testsuite.wamp.ws/case/3.1.2#1`
 * `http://api.testsuite.wamp.ws/case/3.1.2#2`
 * `http://api.testsuite.wamp.ws/case/3.1.2#3`
 * `http://api.testsuite.wamp.ws/case/3.1.2#4`

#### Tested Values

Each *combination* of `value1` and `value2` from the following list:

	[FIXME]


## 3.2 Argument and return types (String)


### 3.2.1 Scalar Value Echo (String)

*Description*

Echo a single scalar value of string type.

*Expectation*

The value is roundtripped exactly.

*Signature*

     (value|string) -> result|string

     value:   The value to be echo'ed back.
     result:  The echo'ed value.

Each of the following endpoints is tested with all test values from below.

#### Tested Endpoints

 * `http://api.testsuite.wamp.ws/case/3.2.1#1`
 * `http://api.testsuite.wamp.ws/case/3.2.1#2`
 * `http://api.testsuite.wamp.ws/case/3.2.1#3`
 * `http://api.testsuite.wamp.ws/case/3.2.1#4`

#### Tested Values

Each value from the following list of strings:

       ["", " ", "\t", "\n", "hello", " hello", "hello ", u"Hello-µ@ßöäüàá-UTF-8!!"]

Each value from the list of UTF8 strings generated by

	autobahntestsuite.case.case6_x_x.createValidUtf8TestSequences()



## 3.4 Argument and return types (Boolean)

### 3.4.1 Scalar Value Echo (Boolean)

*Description*

Echo a single scalar value of boolean type.

*Expectation*

The value is roundtripped exactly (or semantically equivalent).

*Signature*

     (value|bool) -> result|bool

     value:   The value to be echo'ed back.
     result:  The echo'ed value.

Each of the following endpoints is tested with all test values from below.

#### Tested Endpoints

 * `http://api.testsuite.wamp.ws/case/3.4.1#1`
 * `http://api.testsuite.wamp.ws/case/3.4.1#2`

#### Tested Values

Each `value` from the following list:

	[false, true, null, 0, 1, 2, -2]


### 3.4.2 XOR (Boolean)

*Description*

XOR two scalar values of boolean type.

*Expectation*

The correct (XORed) value is returned.

*Signature*

     (value1|bool, value2|bool) -> result|bool

     value1:  The first boolean value.
     value2:  The second boolean value.
     result:  value1 XOR value2.

Each of the following endpoints is tested with all test values from below.

#### Tested Endpoints

 * `http://api.testsuite.wamp.ws/case/3.4.2#1`
 * `http://api.testsuite.wamp.ws/case/3.4.2#2`

#### Tested Values

Each *combination* of `value1` and `value2` from the following list:

	[false, true, null, 0, 1, 2, -2]