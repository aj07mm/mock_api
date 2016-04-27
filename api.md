FORMAT: 1A
HOST: http://localhost:3000/

# Orama Mock API

A mocked API for the new schema

## Authentication headers

+ x-login - The user login
+ authorization - A password hash

## Attribute reference

+ The coordinates are structured in the following order:

    [lat, lng]

+ The receivedAt attribute

    This field corresponds to the moment the data was received by the STI

## Group Person

A bus person

A person object has the following attributes:

+ id
+ birth_city
+ birth_country
+ birth_state
+ home_address
+ birth_date
+ cpf_cnpj
+ father_name
+ full_name
+ is_father_unknown
+ mailing_address_type
+ marital_status
+ marital_name
+ nationality
+ nationality_other
+ partner_name
+ sex

## List and Create  [/person]

### List All persons [GET]

+ Response 200 (application/json)

    + Headers

            Link: </person?page=2>; rel="next"

    + Body

            [
                {
                    id: 1,
                    birth_city: 1,
                    birth_country: 1,
                    birth_state: 1,
                    home_address: 1,
                    birth_date: "23/23/2322",
                    cpf_cnpj: "123123123123",
                    father_name: "John Doe Father",
                    full_name: "John Doe",
                    is_father_unknown: true,
                    mailing_address_type: 1,
                    marital_status: "não gosto de gente",
                    marital_name: "solitário",
                    nationality: "brasileiro",
                    nationality_other: "não sei",
                    partner_name: "Mary Doe",
                    sex: "male"
                }
            ]

### Create a New person [POST]

You may create your own person using this action. It takes a JSON
object containing a person resource.

+ Request (application/json)

            {
                id: 1,
                birth_city: 1,
                birth_country: 1,
                birth_state: 1,
                home_address: 1,
                birth_date: "23/23/2322",
                cpf_cnpj: "123123123123",
                father_name: "John Doe Father",
                full_name: "John Doe",
                is_father_unknown: true,
                mailing_address_type: 1,
                marital_status: "não gosto de gente",
                marital_name: "solitário",
                nationality: "brasileiro",
                nationality_other: "não sei",
                partner_name: "Mary Doe",
                sex: "male"
            }

+ Response 201 (application/json)

    + Headers

            Location: /person/2

    + Body

            {
                id: 1,
                birth_city: 1,
                birth_country: 1,
                birth_state: 1,
                home_address: 1,
                birth_date: "23/23/2322",
                cpf_cnpj: "123123123123",
                father_name: "John Doe Father",
                full_name: "John Doe",
                is_father_unknown: true,
                mailing_address_type: 1,
                marital_status: "não gosto de gente",
                marital_name: "solitário",
                nationality: "brasileiro",
                nationality_other: "não sei",
                partner_name: "Mary Doe",
                sex: "male"
            }

### Update a person [PUT /person/{id}]


You may update your own person using this action. It takes a JSON
object containing a person resource.

+ Parameters
    + id (required, number, `1`) ... ID of the event in form of an integer

+ Request (application/json)

            {
                id: 1,
                birth_city: 1,
                birth_country: 1,
                birth_state: 1,
                home_address: 1,
                birth_date: "23/23/2322",
                cpf_cnpj: "123123123123",
                father_name: "John Doe Father",
                full_name: "John Doe",
                is_father_unknown: true,
                mailing_address_type: 1,
                marital_status: "não gosto de gente",
                marital_name: "solitário",
                nationality: "brasileiro",
                nationality_other: "não sei",
                partner_name: "Mary Doe",
                sex: "male"
            }

+ Response 201 (application/json)

    + Headers

            Location: /person/2

    + Body

            {
                id: 1,
                birth_city: 1,
                birth_country: 1,
                birth_state: 1,
                home_address: 1,
                birth_date: "23/23/2322",
                cpf_cnpj: "123123123123",
                father_name: "John Doe Father",
                full_name: "John Doe",
                is_father_unknown: true,
                mailing_address_type: 1,
                marital_status: "não gosto de gente",
                marital_name: "solitário",
                nationality: "brasileiro",
                nationality_other: "não sei",
                partner_name: "Mary Doe",
                sex: "male"
            }

## Get and Delete [/person/{id}]

+ Parameters
    + id (required, number, `1`) ... ID of the person in form of an integer

### View a person Detail [GET]

+ Response 200 (application/json)

            {
                id: 1,
                birth_city: 1,
                birth_country: 1,
                birth_state: 1,
                home_address: 1,
                birth_date: "23/23/2322",
                cpf_cnpj: "123123123123",
                father_name: "John Doe Father",
                full_name: "John Doe",
                is_father_unknown: true,
                mailing_address_type: 1,
                marital_status: "não gosto de gente",
                marital_name: "solitário",
                nationality: "brasileiro",
                nationality_other: "não sei",
                partner_name: "Mary Doe",
                sex: "male"
            }

### Delete a person record  [DELETE]

+ Response 200 (application/json)

                {
                    "ok": 1,
                    "n": 1
                }