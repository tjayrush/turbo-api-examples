# Adding Custom Sync Stages

This collection of examples shows you how to do two things:

1. How (and why) to create a custom sync stages for Turbo-Geth, and
2. How (and why) to add your own custom RPC commands.

---

## Important Note

These examples modify the internal workings of Turbo-Geth and therefore may damage existing Turbo-Geth database. **Use with extreme caution.**

It is possible to re-sync the database if you damage it (**which you may**), but you want to avoid this, so be careful (step through your code with a debugger) and use a backup copy of the database (or a testnet). See the Turbo-Geth command line options for information on using a testnet.

## Examples:

---

### Total Supply

The first example, `supply`, adds a custom sync stage exposing the per-block total Ether supply. The data is stored in a newly-created table in Turbo-Geth's internal database. The example also shows you how to add a custom RPC command (`tg_getSupply`) to query the newly-created data.

See the [README.md](./cmd/supply/README.md) for details on building and running the custom stage. See [this readme](https://github.com/ledgerwatch/turbo-geth/tree/master/cmd/rpcdaemon) for information on the `rpcdaemon`.

---

### GasUsed / GasPrice

The second example, `mint`, builds a custom stage that exports `gasUsed` and `gasPrice` into an external CSV data file.

This is a work in progress. **Use with caution!**

See the [README.md](./cmd/mint/README.md) file for more information.
