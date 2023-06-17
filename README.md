Sure, here's the formatted README structure that you can directly copy and paste:

# Boston House Pricing Prediction

This project is a Flask application that deploys a machine learning model to predict house prices in Boston. The project also includes a Docker configuration for easy deployment.

## Software and Tools Requirements

1. [Python 3.7](https://www.python.org/downloads/release/python-370/)
2. [Anaconda](https://www.anaconda.com/products/distribution)
3. [Github Account](https://github.com/)
4. [Heroku Account](https://heroku.com)
5. [VSCode IDE](https://code.visualstudio.com/)
6. [Git CLI](https://git-scm.com/book/en/v2/Getting-Started-The-Command-Line)
7. [Docker](https://www.docker.com/)

## Setting Up The Environment

To create a new environment with Anaconda, run the following command:

```
conda create -p myenv python==3.7 -y
```

After creating the environment, activate it:

```
conda activate myenv
```

Install all the required packages:

```
pip install -r requirements.txt
```

## Application Structure

- `app.py` - The main application script that loads the trained model and runs the Flask server.
- `regmodel.pkl` - The trained regression model for house price prediction.
- `scaling.pkl` - The scaler object used to standardize the features.
- `requirements.txt` - Contains the list of python packages required to run the application.
- `Dockerfile` - Contains instructions to build a Docker image for the application.
- `Procfile` - Used by Heroku to start the application.
- `.gitignore` - Specifies files and directories that should be ignored by Git.
- `README.md` - Provides information about the project, how to set up, and deployment steps.
- `LICENSE` - Defines the license type of the project.
- `project.ipynb` - Jupyter notebook used for the development of the machine learning model.
- `templates/` - Contains HTML templates for the web application.
- `.github/workflows/` - Contains Github actions for continuous integration and deployment.

## Local Deployment

To run the application locally, use the following command:

```
python app.py
```

The application will be accessible at `http://localhost:5000`.

## Docker Deployment

Build the Docker image:

```
docker build -t boston_house_price_prediction .
```

Run the Docker container:

```
docker run -p 5000:5000 boston_house_price_prediction
```

The application will be accessible at `http://localhost:5000`.

## Heroku Deployment

Ensure you have logged into your Heroku account using the CLI:

```
heroku login
```

Create a new Heroku app:

```
heroku create <your-app-name>
```

Push the Docker image to Heroku:

```
heroku container:push web -a <your-app-name>
```

Release the image to your app:

```
heroku container:release web -a <your-app-name>
```

Your application will be accessible at `https://<your-app-name>.herokuapp.com`.

## License

This project is licensed under the Apache License 2.0. For more details, see the [LICENSE](LICENSE) file.

Just replace `<your-app-name>` with the name of your Heroku app in the Heroku deployment section.