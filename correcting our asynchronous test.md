	addressBook.addContact(thisContact);
	addressBook.deleteContact(0);

	expect(addressBook.getContact(0)).not.toBeDefined();
	});
});

describe('Async Address Book', function() {
	var addressBook = new AddressBook();

	beforeEach(function(done) {
		addressBook.getInitalContacs(function() {
		});
	});

	it('should grab inital contacts', function(done) {
		expect(addressBook.initalComplete).toBe(true);
	});
});