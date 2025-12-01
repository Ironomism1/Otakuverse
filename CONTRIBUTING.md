# Contributing to OtakuVerse

Thank you for your interest in contributing to OtakuVerse! We're excited to have you join our community.

## Code of Conduct

We are committed to providing a welcoming and inspiring community for all. Please read and follow our Code of Conduct.

## How to Contribute

### Reporting Bugs

Before creating bug reports, please check the issue list as you might find out that you don't need to create one. When you are creating a bug report, please include as many details as possible:

- **Use a clear and descriptive title**
- **Describe the exact steps which reproduce the problem**
- **Provide specific examples to demonstrate the steps**
- **Describe the behavior you observed after following the steps**
- **Explain which behavior you expected to see instead and why**
- **Include screenshots and animated GIFs if possible**

### Suggesting Enhancements

Enhancement suggestions are tracked as GitHub issues. When creating an enhancement suggestion, please include:

- **Use a clear and descriptive title**
- **Provide a step-by-step description of the suggested enhancement**
- **Provide specific examples to demonstrate the steps**
- **Describe the current behavior and the expected behavior**
- **Explain why this enhancement would be useful**

### Pull Requests

- Fill in the required template
- Follow the Python and TypeScript styleguides
- End all files with a newline
- Avoid platform-dependent code

## Development Setup

### Prerequisites
- Python 3.10+
- Node.js 16+
- Git

### Local Development

1. **Fork the repository**
```bash
gh repo fork Ironomism1/Otakuverse --clone
cd Otakuverse
```

2. **Set up backend development environment**
```bash
python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate
pip install -r requirements.txt
```

3. **Set up frontend development environment**
```bash
cd Frontend
npm install
```

4. **Create a feature branch**
```bash
git checkout -b feature/your-feature-name
```

5. **Make your changes and commit**
```bash
git add .
git commit -m "feat: clear description of your changes"
```

6. **Push to your fork and create a Pull Request**
```bash
git push origin feature/your-feature-name
```

## Styleguides

### Python Code Style

- Follow [PEP 8](https://www.python.org/dev/peps/pep-0008/)
- Use 4 spaces for indentation
- Use type hints where applicable
- Write docstrings for all functions and classes

Example:
```python
def get_recommendations(
    user_id: str,
    genres: List[str],
    moods: List[str],
    limit: int = 10
) -> List[Dict[str, Any]]:
    """
    Get personalized recommendations for a user.
    
    Args:
        user_id: Unique user identifier
        genres: List of preferred genres
        moods: List of user moods
        limit: Maximum number of recommendations
        
    Returns:
        List of recommendation dictionaries
    """
```

### TypeScript Code Style

- Use 2 spaces for indentation
- Use `const` by default, `let` when needed
- Use explicit type annotations
- Use PascalCase for components, camelCase for variables

Example:
```typescript
interface RecommendationProps {
  title: string;
  rating: number;
  genres: string[];
}

const RecommendationCard: React.FC<RecommendationProps> = ({
  title,
  rating,
  genres,
}) => {
  return <div>...</div>;
};
```

### Commit Messages

- Use the present tense ("Add feature" not "Added feature")
- Use the imperative mood ("Move cursor to..." not "Moves cursor to...")
- Limit the first line to 72 characters or less
- Reference issues and pull requests liberally after the first line

Example:
```
feat: add mood mapping intelligence to recommendations

- Implement 8 user mood categories
- Map to 16+ content mood attributes
- Add mood translation tests

Fixes #123
```

## Testing

### Backend Tests
```bash
pytest tests/
pytest tests/test_mood_mapping.py -v
```

### Frontend Tests
```bash
cd Frontend
npm test
```

### Manual Testing

Test the recommendation flow:
```bash
curl -X POST http://127.0.0.1:8001/recommendations \
  -H "Content-Type: application/json" \
  -d '{
    "user_id": "test_user",
    "moods": ["happy"],
    "genres": ["action"],
    "content_types": ["anime"]
  }'
```

## Documentation

- Write clear docstrings for all functions
- Update README.md if you add new features
- Add comments for complex logic
- Include examples in documentation

## Need Help?

- Check out the [main README](README.md)
- Read the [API documentation](otakuverse/README.md)
- Ask in GitHub Issues

## License

By contributing to OtakuVerse, you agree that your contributions will be licensed under its MIT License.

## Recognition

Contributors will be recognized in the README.md file and in GitHub's contributors page.

Thank you for contributing! 🎉
