# Spacing & Rhythm

## Goal

Create clean, readable Android layouts with consistent spacing.

## Rules

- Use an 8dp spacing system.
- Prefer `8.dp`, `12.dp`, `16.dp`, `24.dp`, `32.dp`.
- Use `16.dp` as default screen horizontal padding.
- Use `24.dp` for major section gaps.
- Use `8.dp` or `12.dp` for related item gaps.
- Use `Arrangement.spacedBy()` for repeated spacing.
- Avoid random spacing values like `7.dp`, `13.dp`, `19.dp`.

## Recommended Values

```kotlin
val SpaceXS = 4.dp
val SpaceS = 8.dp
val SpaceM = 16.dp
val SpaceL = 24.dp
val SpaceXL = 32.dp
```

## Good Pattern

```kotlin 
Column(
    modifier = Modifier
        .fillMaxSize()
        .padding(horizontal = 16.dp),
    verticalArrangement = Arrangement.spacedBy(16.dp)
) {
    Header()
    Content()
    PrimaryAction()
}
```

## Avoid

```kotlin 
Column {
    Spacer(modifier = Modifier.height(11.dp))
    Text("Title")
    Spacer(modifier = Modifier.height(27.dp))
}
```

## Checklist
- Are related items close together?
- Are unrelated sections separated clearly?
- Is screen padding consistent?
- Are spacing values predictable?
- Is the layout breathable, not crowded?