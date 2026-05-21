# Form Layouts

## Goal

Create clear, usable, and error-friendly Android form screens.

## Rules

- Group related fields together.
- Use clear labels.
- Show helper text only when useful.
- Show validation errors close to the field.
- Keep primary action visible and easy to reach.
- Avoid too many fields on one screen.
- Use proper keyboard types.
- Support loading and disabled states during submission.

## Good Pattern

```kotlin
Column(
    modifier = Modifier
        .fillMaxSize()
        .padding(16.dp),
    verticalArrangement = Arrangement.spacedBy(16.dp)
) {
    OutlinedTextField(
        value = email,
        onValueChange = onEmailChange,
        label = { Text("Email") },
        isError = emailError != null,
        supportingText = {
            emailError?.let { Text(it) }
        },
        modifier = Modifier.fillMaxWidth()
    )

    Button(
        onClick = onSubmit,
        enabled = !isLoading,
        modifier = Modifier.fillMaxWidth()
    ) {
        Text(if (isLoading) "Please wait..." else "Continue")
    }
}
```

## Avoid
- Placeholder-only fields without labels.
- Error messages shown far from fields.
- Buttons enabled during loading.
- Tiny touch targets.
- Long forms without grouping.
- Business validation logic inside composables.

## Checklist
- Are labels clear?
- Are errors shown near fields?
- Is the submit button visible?
- Is loading state handled?
- Is keyboard type correct?
- Is form state hoisted?