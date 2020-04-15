---
layout: splash
title: "Hotel Visitor Manager"
date: 2020-3-11
author_profile: false
tags: [java, object oriented]
header: Hotel Visitor Manager
excerpt: "Learning how to do object oriented programming"
---
# Hotel Visitor Manager

In my Object Oriented Programming class at university, I was learning the key
concepts behind Java and OOP. For an assignment I had to complete the implementation
of a Hotel Visitor Manager using concepts that I had recently learned.

Specifically in this assignment I was learning the basics behind abstraction
and encapsulation with the use and creation of appropriate classes, objects and
methods that fit with what the client wanted.

Some example of some code can be seen below:

```Java
public class Party {
	// host/visitor detail string arrays
	private String[] _hostDetails = new String[3];
	private String[] _visitorDetails = new String[7];

	// party constructor for host
	public Party(String familyName, String givenName, String email) {
		System.out.println("A Party Object was created - host - for " + givenName + " " + familyName);
		// split host details into string array
		_hostDetails[0] = familyName;
		_hostDetails[1] = givenName;
		_hostDetails[2] = email;
	}

	// party constructor for visitor
	public Party(String familyName, String givenName, String organisation, String visitorEmail,
			String hostEmail, String visitDate, String visitStartTime) {
		System.out.println("A Party Object was created - visitor - for " + givenName + " " + familyName);
		// split host details into string array
		_visitorDetails[0] = familyName;
		_visitorDetails[1] = givenName;
		_visitorDetails[2] = organisation;
		_visitorDetails[3] = visitorEmail;
		_visitorDetails[4] = hostEmail;
		_visitorDetails[5] = visitDate;
		_visitorDetails[6] = visitStartTime;
	}

	public String[] getHostDetails() {
		return _hostDetails;
	}

	public String[] getVisitorDetails() {
		return _visitorDetails;
	}
}
```

I faced a lot of problems understanding how objects were able to 'communicate'
with one another at first and did a lot of troubleshooting centred around
public/private and instance/static methods and fields. Once it clicked, however,
it was not too much work to finish off the assignment.


For more about how the assignment worked, I have the download file in my
GitHub.
