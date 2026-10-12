# Contributing

Thanks for taking the time.

## Where the code lives

The packages published as `@chatlychat/*` are built from a private monorepo
where the rest of the platform, its migrations and its ~130 contract checks
live. That means **a pull request against a package mirror cannot be merged
directly** — but a patch is still the fastest way to get something fixed, and
we will port it with attribution.

So: open an issue, or open a PR and we will treat the diff as the proposal.

## What makes a report easy to act on

- The **exact** request or call, including the package version (`npm ls
@chatlychat/sdk-node`) and the Node or browser version.
- What you expected and what happened. If the API answered, paste the body —
  every error carries a stable `error.code`, and that code is usually enough
  to find the cause.
- For a signature problem: which surface, and the headers you received. Our
  signing schemes differ per surface and the timestamp unit is not the same
  everywhere.

## What we will tell you honestly

If something is a gap rather than a bug, we will say so and say whether it is
planned. If the documentation is wrong, that is a bug and we treat it as one —
several of the most useful reports we have had were "your docs say X and the
API does Y".
