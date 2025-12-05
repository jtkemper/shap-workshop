FROM rocker/binder:4.5.2
LABEL maintainer='John Kemper'
COPY --chown=${NB_USER} . ${HOME}
USER ${NB_USER}



RUN wget https://github.com/jtkemper/shap-workshop/raw/master/DESCRIPTION && R -e "options(repos = list(CRAN = 'http://mran.revolutionanalytics.com/snapshot/2025-12-05/')); devtools::install_deps()"

RUN rm DESCRIPTION.1; exit 0
