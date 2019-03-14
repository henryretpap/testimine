describe('Address book'), function() {
 it('should be able to add a contact', function() {
  var addressBook = new AddressBook(),
   thisContact = new Contact();

	addressBook.addContact(thisContact);
	addressBook.deleteContact(0);

	expect(addressBook.getContact(0)).not.toBeDefined();
  });
});