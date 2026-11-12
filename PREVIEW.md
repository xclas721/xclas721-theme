# xclas721-theme

### Deep teal. Bright mint. A little warmth.

A dark theme for **Orca** — app, code and terminal in one palette.

> A quiet canvas for your next idea.

## The palette

| Deep teal | Mint | Cyan | Peach | Rose |
| :--- | :--- | :--- | :--- | :--- |
| `#002b36` | `#19f9d8` | `#09cbdd` | `#ffcc95` | `#f48fb1` |

## Make something useful

```typescript
// Small steps, clear ideas.
interface Theme {
  name: string;
  accent: string;
  dark: boolean;
}

const theme: Theme = {
  name: "xclas721-theme",
  accent: "#19f9d8",
  dark: true,
};

function welcome(name: string): string {
  return `Ready to build, ${name}?`;
}

console.log(welcome(theme.name));
```

**Mint accents** · *Soft comments* · `Matching terminal colors`

[xclas721 / xclas721-theme](https://github.com/xclas721/xclas721-theme) · MIT · Made for Orca
