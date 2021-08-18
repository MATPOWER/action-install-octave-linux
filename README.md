Install Octave (Linux)
======================

### GitHub Action to install [GNU Octave][1] on Linux

Installs [GNU Octave][1] on Linux runners and sets the following environment
variables.
- `IS_MATLAB` set to 0
- `IS_OCTAVE` set to 1
- `ML_CMD` set to `octave-cli --no-gui --eval`
- `ML_PATHVAR` set to `OCTAVE_PATH`
- `OCTAVE_VER` set to the version of [Octave][1] installed

### Optional Input

- `ipopt-libs` - (default `false`) set to `true` to include installation
  of IPOPT libraries

### Example Usage
```
    steps:
    - name: Install Octave
      uses: MATPOWER/action-install-octave-linux@v1
      with:
        ipopt-libs: true

    - name: Octave ${{ env.OCTAVE_VER }} Installed
      run: $ML_CMD ver
```

[1]: https://octave.org
