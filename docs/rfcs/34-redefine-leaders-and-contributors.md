- Author: Xuanwo <github@xuanwo.io>
- Start Date: 2021-08-18
- RFC PR: [beyondstorage/community#34](https://github.com/beyondstorage/community/pull/34)
- Tracking Issue: [beyondstorage/community#0](https://github.com/beyondstorage/community/issues/0)

# RFC-34: Redefine Leaders and Contributors

Previous Discussion:

- [proposal: Separating Leaders](https://github.com/beyondstorage/community/issues/26)

## Background

In [GSP-128], we defined our community organization to make it clear that everyone's rights and responsibilities. After sometime evaluation, we find out some shortcomings.

- Levels are too much: we have 5 roles for every project.
- `Leader` is not used: `Maintainer` is responsible for the whole project
- `Contributor` is meaningless for a single project.

## Proposal

So I propose to implement the following changes:

- Remove `Leader` role from single projects
- Remove `Contributor` role from single projects

Instead, we will add:

- `PMC` (Project Management Committee) for the whole BeyondStorage community.
  - PMC will be the management team for BeyondStorage, involved in the roadmap development of major community-related resolutions.
  - PMC will have `admin` permission for all repos under BeyondStorage.
- `Contributor` for the whole BeyondStorage community.
  - We will use community contributors instead of project contributors.

After these changes, our organization layout will be:

```txt
   ┌────────────────────────────────────────────────┐
   │                     PMC                        │
   └────────────────────────────────────────────────┘
   ┌─────────────┐  ┌──────────────┐  ┌─────────────┐
   │  beyond-tp  │  │  go-storage  │  │  community  │
   │             │  │              │  │             │
   │  Committer  │  │   Committer  │  │  Committer  │
   │  Reviewer   │  │   Reviewer   │  │  Reviewer   │
   └─────────────┘  └──────────────┘  └─────────────┘
   ┌────────────────────────────────────────────────┐
   │                   Contributor                  │
   └────────────────────────────────────────────────┘
```


## Rationale

N/A

## Compatibility

N/A

## Implementation

All changes will be reflected in [go-community](https://github.com/beyondstorage/go-community)

[GSP-128]: https://github.com/beyondstorage/go-storage/blob/master/docs/rfcs/128-community-organization.md
