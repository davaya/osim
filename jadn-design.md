# JSON Abstract Data Notation (JADN)

## Design
According to RFC 3444, the main purpose of an IM is to model managed objects
at a conceptual level, independent of any specific implementations or protocols
used to transport the data.
IMs can be defined in an informal way, using natural languages such as English.
Alternatively, IMs can be defined using a formal language or a semi-formal
structured language.

JADN is a formal language that unambiguously defines information types and
classifies data values as instances of a type, based on the following
design principles:

### Information-Centric
An information model can be information-centric or data-centric. JADN is
designed from the ground up to be information-centric: its core types
are based on required behavior of the internal representations of those
types, as opposed to data instances. A JADN IM can be used at the
conceptual design stage without involving any serialization. Conceptual
designs are often expressed as entity relationship diagrams, OOP class
diagrams, property tables, or domain-specific text languages. Because
JADN can generate these artifacts, they precisely represent the IM,
as opposed to being source material from which an IM is created by hand.

A data-centric IM might not exist except in serialized form, and
transitioning from conceptual to formal IM may be less straightforward.

**Examples:**

JADN defines two numeric core types:
* Integer types are whole numbers of any precision
* Number types are real (rational and irrational) numbers

Data-centric information models define core types in terms of strings:
* decimal represents a subset of the real numbers, which can be represented
by decimal numerals
* integer is derived from decimal by fixing the value of fractionDigits
to be 0 and disallowing the trailing decimal point

An information-centric IM does not have date- or time-related core types;
dates and times are represented internally by a numeric offset from a
base value, and externally by an an unlimited number of date/time formats.
There is a single Binary core type for the set of finite-length sequences
of binary octets, which can be serialized directly as binary data in
addition to multiple string formats.

A data-centric IM defines a number of date- and time-related string types,
such as dateTime, date, time, gYearMonth, gMonthDay, etc.
There are two core types for binary data: hexBinary and base64Binary, both
of which are the set of finite-length sequences of binary octets.

### Minimum Set of Core Types


### Extensions

### Datatypes

### Information Graph

