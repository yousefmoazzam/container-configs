FROM ghcup:0.0.1

# [Choice] GHC version: recommended, latest, 9.2, 9.0, 8.10, 8.8, 8.6
ARG GHC_VERSION="recommended"

# Use GHCup to install versions of main utilities
# If you prefer to let the Haskell extension install everything on demand,
# comment out the lines below. In that case, you may need to manually run "cabal update""."
RUN ghcup install ghc "${GHC_VERSION}" --set
RUN ghcup install cabal recommended --set
RUN ghcup install hls recommended --set
RUN cabal update

# Code formatter
RUN cabal install ormolu
