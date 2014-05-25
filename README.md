Address Book v3
================

February 26, 2014

Epicodus: Week2, Day3

Object-oriented JS, continuning with BDD/TDD

*******************
Lesson: address book with better functionality for addresses, phone numbers, and contacts

Address Book

To start today off, follow along with the video and implement the initialize() and create() methods on Contact.

Next, refactor the Address object to have initialize() and create() methods, just like the Contact object now has. Make sure to use the BDD process as you go!

Now, wouldn't it be nice if you could create an instance of Address and it automatically was added to the proper contact? Make these two specs pass:

specs.js

    describe("Contact", function() {
      describe("createAddress", function() {
        it("creates an address object", function() {
          var testContact = Contact.create();
          var testAddress = testContact.createAddress();
          Address.isPrototypeOf(testAddress).should.equal(true);
        });
    
        it("adds the address to the addresses property of the contact", function() {
          var testContact = Contact.create();
          var testAddress = testContact.createAddress();
          testContact.addresses.should.eql([testAddress]);
        });
      });
    });

Update your user interface code to use the new createAddress() method you just wrote.

Write similar methods to the above ones for phone numbers.

