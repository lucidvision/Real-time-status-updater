## Features to Add

### Asynchronous updates

The statuses in the UI should update asynchronously, in close to realtime,
without having to refresh the page or click the update link.

### Teams

The app should be able to support teams of users (such as Customer Service
Reps, Salespeople) so that people on a team can better track the people
they work with.

A user can only belong to a single team. The following functionality should
be present:

  * Create a team
  * Delete a team
  * Change a team's name
  * Add & remove people from teams

### Tests

Ensure that the app has good test coverage using RSpec. Your tests should
produce a reasonable test coverage report. (Use `COVERAGE=true bundle exec
rspec` to generate the coverage report; the report is located at
`coverage/index.html`.)

### Migration for IP addresses

There is a branch in this project (`integer-ips-for-users`) which contains
code to convert the `current_sign_in_ip` and `last_sign_in_ip` columns on
the User table from strings to integers. Merge it into your code.

This branch contains a migration
(`20130416230652_convert_string_ips_to_integers.rb`) which, when run, will
destroy any existing data in those columns. Alter this migration to ensure
that, if the database was full of data before the migration, all data would
still be intact afterwards.
