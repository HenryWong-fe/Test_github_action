    - name: Deploy to Server
      uses: easingthemes/ssh-deploy@v2.0.2
      env:
        SSH_PRIVATE_KEY: ${{ secrets.SERVER_SSH_KEY }}
        ARGS: "-rltgoDzvO --delete"
        SOURCE: "dist/"
        REMOTE_HOST: ${{ secrets.REMOTE_HOST }}
        REMOTE_USER: ${{ secrets.REMOTE_USER }}
        TARGET: ${{ secrets.REMOTE_TARGET }}    