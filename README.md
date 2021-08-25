Install Octave (Linux)
======================

### GitHub Action to install [GNU Octave][1] on Linux

Installs [GNU Octave][1] on Linux runners and sets the following environment
variables.
- `OCTAVE_VER` set to the version of [Octave][1] installed
- `ML_NAME` set to `Octave`
- `ML_VER` set to same as `OCTAVE_VER`
- `ML_CMD` set to `octave-cli --no-gui --eval`
- `ML_PATHVAR` set to `OCTAVE_PATH`

### Optional Input

- `ipopt-libs` - (default `false`) set to `true` to include installation
  of IPOPT libraries

### Outputs

None.

### Example Usage
```
    steps:
    - name: Install Octave
      uses: MATPOWER/action-install-octave-linux@v1
      with:
        ipopt-libs: true

    - name: Octave ${{ env.ML_VER }} Installed
      run: $ML_CMD ver
```

[1]: https://octave.org
