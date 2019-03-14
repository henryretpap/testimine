	addressBook.addContact(thisContact);
	addressBook.deleteContact(0);

	expect(addressBook.getContact(0)).not.toBeDefined();
	});
});

describe('Async Address Book', function() {
	it('Should grab initial contacts', function() {
		var addressBook = new AddressBook();

		addressBook.getInitalContacts();
		expect(addressBook.initalComplete).toBe(true);
	});
});