# Reproduction for https://github.com/rcarriga/vim-ultest/issues/31

1. Run `yarn`
2. Open Neovim in the root directory
3. Open `packages/app/src/test_does_not_work.spec.ts`
4. Run `Ultest` there
5. Notice there's no output

To "fix" it:

1. Add test dependencies to the root of the repo (this is a bad idea): `yarn add -W -D jest typescript @types/jest`
2. Confirm that the test suite now works
