- Author: Xuanwo <github@xuanwo.io>
- Start Date: 2021-09-23
- RFC PR: [beyondstorage/community#0](https://github.com/beyondstorage/community/issues/0)
- Tracking Issue: [beyondstorage/community#0](https://github.com/beyondstorage/community/issues/0)

# RFC-0: Community Merge

Pre-Proposal: <https://forum.beyondstorage.io/t/topic/241>

## Background

We host our real-time communication as matrix.org, and then bridge them to slack, telegram, and so on. However, we created too many rooms, and most of them only have two or three persons. Even worse, we also created many `xxx-zh` rooms for chinese speaking discussion.

Both of them have divided our community into countless small parts.

## Proposal

So I propose to merge our community together.

### Merge all `*-zh` groups into `zh-hans`

We will have only one language-specified room instead of a `*-zh` group for every project.

And in the further, we will host rooms like `zh-hant`, `ru` and so on.

### Merge all `go-service-*` groups into `go-storage`

Our original plan was to avoid extraneous messages affecting too many people, but that ended up with only two or three people per chat, which did not work as expected.

Merge all our service rooms into `go-storage` will resolve this problem.

---

After all those merging, we will have:

- campfire
- go-storage
- beyond-tp
- gsp-xxx
- zh-hans(zh-hant, ru and so on)

## Rationale

N/A

## Compatibility

N/A

## Implementation

We will migrate all our users into corresponding rooms.
