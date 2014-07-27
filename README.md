audit
=====

PoC - don't Use in production. [Create a set of modules to enable a correct audit process on your data over 100% of Odoo]

Plan:
=====

Using this [approach](https://wiki.postgresql.org/wiki/Audit_trigger) try to create a module which enabling properties in a class create the audit sql trigger that can be used to trace the elements CRUD features in a database.

##Technical Consideration to affront the objective:

0. Verify Options already done for proffesional database servers, like Oracle, MySql, MSsql and so on, something may be is done already.
1. The First Approach should be done using Pure SQL to be able to design a correct approach using Odoo.
2. The element on the class must be able to activate by code python and by graphical interface.
3. The result of auditory needs to be Human Readable but not necesary created Human readable (for performance issues).

##Known Limitations:

1. Postgres has only one connection when Odoo is connected with it, then the User which made the change may be is not possible use the approach above, but we should be able to plan an approach that give to postgrs this information (the Odoo User Connected).
2. The SELECT can be traced, but as you cas supose it can be so consuming in terms of performance.
3. It is NOT a replacement of the new approach of "use Actions" on odoo v8.0, It is complementary.

##One time the PoC is finished:

1. The Auditory must be configurable by domain, this Domain must be using the domain approach of Odoo.
2. Due to performance and db size, the approach must to be done in a ways that even may be need to use a different DB, Different tables and so on with this we can ensure that a BKP will not have "Always" the Audory Schema.
