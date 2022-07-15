# Trigger Take Away

# Error: DML statement cannot operate on Trigger.new or Trigger.old

```
Solution: Remove the update DML statement at the end. By using the "before" trigger to modify the Trigger.new objects, you don't need to explicitly perform an update DML statement. When the trigger ends, it will implicitly update the data as you have modified the values.

Explanation: Trigger.old represents the data as it was loaded from the database. It does not represent data that will be saved to the database. As such, it is immutable (cannot be modified). Trigger.new reflects what the database will look like; in a before DML event, you can modify these values to alter what will be saved to the database, but in after DML events, the data is already saved and cannot be modified further (by code, anyways, as Workflow Rules can cause a recursive update).

Within a trigger context, it is an error to attempt to perform DML on records already in that context, with the presumption that it will cause an infinite loop. Salesforce prevents doing this casually by restricting DML operations on any record in Trigger.old or Trigger.new. It's still possible to engineer a workaround, but in any event, each record may only be involved in a single insert, update, delete, and undelete context at a time; if you try to perform another DML of the same type while you're already processing that record, you'll get an immediate recursion error

```
