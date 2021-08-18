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
   │ Maintainer  │  │  Maintainer  │  │  Maintainer │
   │ Committer   │  │  Committer   │  │  Committer  │
   │ Reviewer    │  │  Reviewer    │  │  Reviewer   │
   └─────────────┘  └──────────────┘  └─────────────┘
   ┌────────────────────────────────────────────────┐
   │                   Contributor                  │
   └────────────────────────────────────────────────┘
```

Since this RFC, we will adopt new process for nominate new contributors or other roles.

- New PMC members should be nominated by existing PMC members.
- New `Maintainer` should be nominated by PMC members.
- New `Committer` and `Reviewer` should be nominated by project `Maintainer`.
- New `Contributor` will be added automatically via tools.

All nomination should be submitted via RFCs.

## Rationale

### Why Contributor is meaningless for a single project but meaningful for the community?

Because `Contributor` in the community will have permission to run integration tests. But contributors for a single project doesn't have special permission other than read.

### PR nomination is enough?

It's an idea that came from tikv community: https://github.com/tikv/community/blob/master/votes/0139-kennytm-as-tikv-committer.md

In the future, we will introduce vote too and PR is hard to record that information. (We have to check every PR)

It will not add too much burden:

- As contributor will be added by tools, the nomination will be a low-frequency operation.
- PR nomination still needs to update teams.toml, camp up with a more detailed RFC is more formal to us.

## Compatibility

N/A

## Implementation

All changes will be reflected in [go-community](https://github.com/beyondstorage/go-community)

[GSP-128]: https://github.com/beyondstorage/go-storage/blob/master/docs/rfcs/128-community-organization.md
