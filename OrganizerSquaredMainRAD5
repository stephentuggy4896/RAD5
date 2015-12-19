var OrganizerSquaredMainRAD5 = {
    appName: 'OrganizerSquaredRAD5',
    userFriendlyAppName: 'Organizer Squared (RAD5 version)',
    defaultLocale: 'en',
    authentication: ['RAD5DefaultFormsAuthentication', 'OAuth2', 'OpenID'],
    authorization: ['dedicatedDbPerOrganizationOrUser'],
    auditTrail: {
        auditOperations: ['create', 'update', 'delete'],
        auditUsing: 'dedicatedTablePerDb'
    },
    modelObjects: {
        Contact: {
            abstractObject: true,
            showInNavigation: true,
            fields: {
                ContactName: {
                    dataType: 'string',
                    required: true,
                    emptyStringAllowed: false,
                    whiteSpaceOnlyAllowed: false
                },
                MemberOfGroups: {
                    dataType: 'Array of reference to ContactGroup',
                    required: false
                },
                PhoneNumbers: {
                    dataType: 'Array of reference to PhoneNumber',
                    required: false
                },
                EmailAddresses: {
                    dataType: 'Array of reference to EmailAddress',
                    required: false
                },
                IMNames: {
                    dataType: 'Array of reference to IMName',
                    required: false
                },
                PostalAddresses: {
                    dataType: 'Array of reference to PostalAddress',
                    required: false
                },
                WebAddresses: {
                    dataType: 'Array of reference to WebAddress',
                    required: false
                },
                OtherContactMethods: {
                    dataType: 'Array of reference to ContactMethod',
                    required: false
                },
                ContactNotes: {
                    dataType: 'string',
                    required: false,
                    emptyStringAllowed: false,
                    whiteSpaceOnlyAllowed: true
                }
            },
            additionalFieldsAllowed: true
        },
        Person: {
            inheritsFrom: 'Contact',
            showInNavigation: true
        },
        ContactGroup: {
            inheritsFrom: 'Contact',
            showInNavigation: true,
            fields: {
                GroupMembers: {
                    dataType: 'Array of reference to Contact',
                    required: false
                }
            }
        },
        ContactMethod: {
            abstractObject: true,
            showInNavigation: false,
            fields: {
                ContactMethodType1: {
                    dataType: 'lookup',
                    required: true,
                    lookupValues: [
                        'Home',
                        'Personal',
                        'Work',
                        'Nonprofit/Volunteer',
                        'Main'
                    ],
                    otherValuesAllowed: true
                },
                ContactMethodNotes: {
                    dataType: 'string',
                    required: false,
                    emptyStringAllowed: false,
                    whiteSpaceOnlyAllowed: true
                }
            }
        },
        PhoneNumber: {
            inheritsFrom: 'ContactMethod',
            showInNavigation: false,
            fields: {
                PhoneNumberType: {
                    dataType: 'lookup',
                    required: true,
                    lookupValues: [
                        'Mobile',
                        'Landline',
                        'VoIP',
                        'Fax',
                        'Pager',
                        'Satellite'
                    ],
                    otherValuesAllowed: true
                },
                CountryCode: {
                    dataType: 'string',
                    maxLength: 5,
                    required: true
                },
                AreaOrCityCode: {
                    dataType: 'string',
                    maxLength: 5,
                    required: true
                },
                Number: {
                    dataType: 'string',
                    maxLength: 20,
                    required: true
                },
                Extension: {
                    dataType: 'string',
                    maxLength: 20,
                    required: false
                }
            }
        }
    }
};
