START PROJECT :

npx nx run app-name:serve:development

CREATE LIBS :

- npx nx g lib libs-name --publishable
  #test:
- npx nx g lib jf-libs-fire --publishable --importPath="jf-libs-fire"

CREATE APP :

- npx nx g app libs-name

DELETE :

- npx nx generate @nrwl/workspace:remove libs-name --no-interactive --dry-run

PUBLISH ANGULAR EXEMPLE:

- https://nx.dev/structure/buildable-and-publishable-libraries
- https://tane.dev/2020/05/publishing-npm-libraries-using-nx-and-github-actions

- npx nx g @nrwl/node:library --name=design-system --publishable --importPath="jf-test-3"

GRAPH:

- npx nx graph

RUNNING TARGETS ON ALL PROJECTS IN THE WORKSPACE:

- npx nx run-many --target=build --all

BUILD LIB:

- npx nx build lib-name

---

### PUBLISH :

npx nx g @nrwl/js:lib test-publish --publishable --importPath="@jfps/jfps-components"
npx nx publish test-publish --ver=1.0.3 --tag=hello
