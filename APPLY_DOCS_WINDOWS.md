# Jak zastosować tę paczkę w repozytorium

## 1. Rozpakuj ZIP

Rozpakuj paczkę dokumentacji obok lokalnego repozytorium projektu.

## 2. Wejdź do repozytorium

```powershell
cd "SCIEZKA_DO_REPO"
```

## 3. Utwórz branch

```powershell
git checkout main
git pull
git checkout -b docs/full-polish-audio-amplifier-docs
```

## 4. Skopiuj pliki

Jeżeli paczka jest rozpakowana obok repozytorium:

```powershell
robocopy "..\wzmacniacz_3w_full_polish_docs" "." /E
```

Kod wyjścia `1` z `robocopy` zwykle oznacza, że pliki zostały poprawnie skopiowane.

## 5. Commit i push

```powershell
git status
git add README.md docs assets CHANGELOG.md .gitignore
git commit -m "Add full Polish amplifier documentation"
git push -u origin docs/full-polish-audio-amplifier-docs
```

## 6. Otwórz Pull Request

Na GitHubie otwórz PR do `main`.
