# Alignment & Hierarchy

## Goal

Make the UI easy to scan, visually balanced, and action-focused.

## Rules

- Align related content to the same edge.
- Prefer start alignment for text-heavy screens.
- Center alignment only for empty states, onboarding, and simple hero sections.
- Use typography size, weight, spacing, and color to create hierarchy.
- Make the primary action visually stronger than secondary actions.
- Keep one clear visual focus per screen.

## Typography Hierarchy

Recommended order:

1. Screen title
2. Section title
3. Body text
4. Supporting text
5. Caption/helper text

## Good Pattern

```kotlin
Column(
    modifier = Modifier.padding(16.dp),
    horizontalAlignment = Alignment.Start
) {
    Text(
        text = "Upgrade to Premium",
        style = MaterialTheme.typography.headlineMedium
    )

    Text(
        text = "Unlock all advanced tools.",
        style = MaterialTheme.typography.bodyMedium,
        color = MaterialTheme.colorScheme.onSurfaceVariant
    )
}
```

Avoid
- Mixing too many alignments on one screen.
- Making all text the same size and weight.
- Center-aligning long paragraphs.
- Placing the CTA far from the main content.
- Using color alone to show importance.

Checklist
- Is the most important content obvious?
- Is text alignment consistent?
- Is the CTA easy to find?
- Is secondary content visually softer?
- Is the screen easy to scan in 3 seconds?